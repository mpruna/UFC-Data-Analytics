v# UFC-Data-Analytics

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


PPV and attendance:
* https://data.world/atseng92/ufc-disclosed-ppv-and-attendance-data-1993-2017

Fighter Social Media:
* https://data.world/johayes13/ufc-fighters-social-media

