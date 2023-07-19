## Have I Been Pwned? Yes

We query [HIBP](https://haveibeenpwned.com/) with emails from the [Florida voter registration database](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/UBIG3F) to estimate how often people's data have been breached. We find that a voter's email in the voter registration database is part of 7.5 breaches on average. The median is 6. The percentage of people whose accounts have been breached is  99.8%. The average number of serious breaches, e.g., breaches where sensitive data like audio recordings, drug habits, photos, etc., associated with the email is 4.5 and the median is 4. Given that data from only a small sliver of breaches are public and given that these breaches are related to one email (people often have multiple addresses), the total number is likely much higher.


|       |   total_breaches |   serious_breaches |   non_fab_breaches |   non_null_uniques |\n
|:------|-----------------:|-------------------:|-------------------:|-------------------:|\n
| count |     335971       |       335971       |       335971       |       335971       |\n
| mean  |          7.54622 |            4.50826 |            7.5462  |            7.54622 |\n
| std   |          5.84812 |            4.0904  |            5.84799 |            5.84812 |\n
| min   |          0       |            0       |            0       |            0       |\n
| 25%   |          3       |            2       |            3       |            3       |\n
| 50%   |          6       |            4       |            6       |            6       |\n
| 75%   |         11       |            6       |           11       |           11       |\n
| max   |        344       |          298       |          344       |          344       |


### Digital Divide: Sociodemographic Predictors of Breaches

The total number of breaches rises sharply from an average of 4 to an average of 7.5 between 20 and 50 years before tapering to around 6. This trend may reflect a combination of things: 1. total number of online accounts (which plausibly increases with age till you reach people who were too old to sign up for too many services), 2. digital savviness, which may be greatest among the youngest. ([Winsorizing](figs/age_winsorized_breaches.png) doesn't change the pattern much.)

The differences across sex and race/ethnicity are not very stark. The difference between the median number of breaches for men and women is 1 with women suffering from more breaches. For race/ethnicity, NH White have a higher median (7) than other racial groups (6).

<img src = "figs/age_breaches.png" width = 500px>


**Total Breaches by Self-Identified Gender**


|    | gender   |   count |   mean |   std |   min |   25 |   50 |   75 |   max |\n
|---:|:---------|--------:|-------:|------:|------:|-----:|-----:|-----:|------:|\n
|  1 | F        |  177919 |    7.7 |   5.7 |     0 |    3 |    7 |   11 |   344 |\n
|  2 | M        |  153259 |    7.4 |   6   |     0 |    3 |    6 |   10 |   344 |\n


**Total Breaches by Self-Identified Race**

|    | race        		|   count |   mean |   std |   min |   25 |   50 |   75 |   max |\n
|---:|:-----------------|--------:|-------:|------:|------:|-----:|-----:|-----:|------:|\n
|  0 | Asian            |    8069 |    7.2 |   5.8 |     0 |    3 |    6 |   10 |   154 |\n
|  1 | Hispanic         |   65438 |    7.3 |   5.7 |     0 |    3 |    6 |   10 |   344 |\n
|  2 | Multi-Racial     |    2623 |    7.2 |   5.4 |     0 |    3 |    6 |   10 |    53 |\n
|  3 | NH Black         |   51089 |    7.2 |   5.9 |     0 |    3 |    6 |   10 |   344 |\n
|  4 | NH White         |  193429 |    7.8 |   5.9 |     0 |    3 |    7 |   11 |   344 |\n
|  5 | Native Americans |     876 |    7.3 |   5.5 |     0 |    3 |    6 |   10 |    42 |\n
|  6 | Other            |    8706 |    7.5 |   5.6 |     0 |    3 |    6 |   11 |    55 |\n
|  7 | Unknown          |    5741 |    6.7 |   5.9 |     0 |    3 |    5 |    9 |   195 |


## Scripts

* [Get Emails from Florida Voter DB](notebooks/01_fl_dat.ipynb)
* [Valid Email Or Not](notebooks/01a_valid_email_or_not.ipynb)
* [Get HIBP Data](notebooks/02_get_fl_hibp.ipynb)
* [Analyze](notebooks/03_concat_fl_dat_analyze.ipynb)

## Reference

Please see also:

1. https://gsood.com/research/papers/pwned.pdf
2. https://github.com/themains/bad_domains


