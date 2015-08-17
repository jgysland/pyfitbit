# pyfitbit
There are other python packages on github (and elsewhere) for scraping data from fitbit.com, but I had mixed results, especially with "intra-day" data, and especially on heart-rate data. So I wrote this. YMMV.

## Usage
```
import pyfitbit

my_data = get_fitbit_data('gimmemy@data.plz', 'andplzdonotsueme', '2015-08-14', '2015-08-17')

print my_data.loc[my_data.bpm > 0].head()

# output
                     distance  active-minutes  bpm  floors  steps   activityLevel  calories-burned
dateTime                                                                                          
2015-08-14 11:00:00  0.000000               0   86       0      0       SEDENTARY         21.03480
2015-08-14 11:15:00  0.034443               0   87       0     75  LIGHTLY_ACTIVE         29.09814
2015-08-14 11:30:00  0.122149               0   92       0    266  LIGHTLY_ACTIVE         48.61376
2015-08-14 11:45:00  0.122603               0   92       2    267  LIGHTLY_ACTIVE         53.98932
2015-08-14 12:00:00  0.015149               0   84       0     33  LIGHTLY_ACTIVE         26.99466
```