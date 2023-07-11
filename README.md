## Have I Been Pwned? Yes

We query [HIBP](https://haveibeenpwned.com/) with emails from the [Florida voter registration database](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/UBIG3F) to estimate how often people's data have been breached. We find that a voter's email in the voter registration database is part of 7 breaches on average. The median is 6. The percentage of people whose accounts have been breached is 100%. The average number of serious breaches, e.g., breaches where sensitive data like audio recordings, drug habits, photos, etc., associated with the email is 4 and the median is 3. Given that data from only a small sliver of breaches are public and given that these breaches are related to one email (people often have multiple addresses), the total number is likely much higher.

* [Get Emails from Florida Voter DB](notebooks/01_fl_dat.ipynb)
* [Get HIBP Data](notebooks/02_get_fl_hibp.ipynb)
* [Analyze](notebooks/03_concat_fl_dat_analyze.ipynb)

## Reference

Please see also: https://gsood.com/research/papers/pwned.pdf
