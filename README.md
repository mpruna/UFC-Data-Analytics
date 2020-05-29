# UFC-Data-Analytics

![IMG](Images/newplot(1).png)
![IMG](Images/newplot(2).png)
![IMG](Images/newplot(3).png)
![IMG](Images//newplot(4).png)


### Project Structure

```
└── datasets
│   ├── UFC_PPV_Data.xlsx
│   └── UFC_Social.xlsx
├── README.md
├── read_ufc_data.ipynb
└── ufcdata
    ├── data.csv
    ├── preprocessed_data.csv
    ├── raw_fighter_details.csv
    └── raw_total_fight_data.csv
```

Analytics on UFC data provided by OpenData. There is another UFC dataset on Kaggle.
ATM checking dataset from OpenData

### To Dos

- [ ] Change data types(date and numeric) some columns have str type
- [ ] Handle null values
- [ ] Analyze

### Change string to float

```
social_stats['Twitter']=pd.to_numeric(social_stats['Twitter'], errors='coerce', downcast='integer')
social_stats['Instagram']=pd.to_numeric(social_stats['Instagram'], errors='coerce', downcast='integer')
```

### Twitter
 
```
social_stats['Twitter'].describe()
count    1.590000e+02
mean     3.344525e+05
std      1.110623e+06
min      1.650000e+02
25%      1.225000e+04
50%      5.250000e+04
75%      2.105000e+05
max      7.860000e+06
Name: Twitter, dtype: float64

```

### Instagram

```
social_stats['Instagram'].describe()

count    1.610000e+02
mean     8.864659e+05
std      3.555651e+06
min      4.852000e+03
25%      2.830000e+04
50%      1.270000e+05
75%      5.860000e+05
max      2.970000e+07
Name: Instagram, dtype: float64
```

| Columns | Description |
|--- | ---|
|fighter_name | Name of the fighter |
|Height | Height in inches |
|Reach | Figher arm lenght |
|Stance| Sauthpaw if fighter is left handed, orthodox if is right handed|
|DOB| Date of Birth |

Before we dive into more details, we have to some common concept related to data analytics.
We can split the data types into three main categories: 

| Data Type | Explanation |
|---|---|
|Numerical | Integer/Float numbers(3.7;7,3) etc|
|Categorical| Data can be split into chategories; ex Southpaw/Orthodox)|  
|Ordinal | data is categorical, but can be measured (tall vs small; fat vs skinny)|


A distinction must be made between the sample and the population. A population from an analytics standpoint refers to all the elements from a set of data. A sample refers to a group of data, a subset of the data. 
The term population does not have a census connotation. We might have mice, engines, movies, cars. Specific to our data set, a sample data might be champion fighters, southpaw fighters.

### Upgrade Plotly

New plotly version is available:

```
conda update plotly
pip install -U plotly
```
### Supported methods:
```
The Plotly backend supports the following kinds of Pandas plots: scatter, line, area, bar, barh, hist and box, via the call pattern df.plot(kind='scatter') or df.plot.scatter(). These delegate to the corresponding Plotly Express functions.
```

PPV and attendance:
* https://data.world/atseng92/ufc-disclosed-ppv-and-attendance-data-1993-2017

Fighter Social Media:
* https://data.world/johayes13/ufc-fighters-social-media

