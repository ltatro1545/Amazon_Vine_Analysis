# Amazon_Vine_Analysis

Resources:
  - Pandas in Python
  - PySpark in Google Colab
  - AWS RDS (Amazon Web Services Relational Database Service)
  - PostgreSQL in pgAdmin 4
  - File used for analysis (outdoor products): https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Outdoors_v1_00.tsv.gz

## Overview
The purpose of this analysis was to determine if there was a bias between the paid Amazon Vine reviewers and the unpaid unaffiliated. Since the datasets were a few hundred megabytes in size, this was an opportunity to utilize PySpark to simulate handling big data. The data was extracted using Pyspark, then transformed, and loaded into a PostgreS database. One data type in particular needed to be changed from a string format to a date-time format. The four tables in PostgreS were subsequently exported as csv files to be used in Pandas.

## Results
The following is an overview of the results:
  - Total reviews
    - Vine reviews: 107
    - Non-Vine reviews: 39,869
  - 5-star reviews
    - Vine reviews: 56
    - non-Vine reviews: 21,005
  - Percent 5-star reviews
    - Vine reviews: 52.34%
    - non-Vine reviews: 52.69%
 
 ![df_setup](https://user-images.githubusercontent.com/92493572/154827266-232bc07e-4bdf-4897-9d71-d28adfe411af.png)

### Screenshot of Paid Results
![paid_results](https://user-images.githubusercontent.com/92493572/154827327-2725bb1e-84b5-4946-a80c-412e1e255500.png)

### Screenshot of Unpaid Results
![unpaid_results](https://user-images.githubusercontent.com/92493572/154827334-c74ea319-e421-4efb-9f53-a1363db02591.png)

## Summary
Given the results of this analysis, at this time it appears both parties provide a similar 5-star rating frequency. To further this anaylsis, a rating distribution should be constructed to better understand all of the reviews - rather than just the highest. This distribution could be charted very easily within matplotlib, which would provide insight as to *how* each party rates overall. Additionally, is there any incentive for Vine reviewers to rate higher? This could create a conflict of interest; Although this surface-level analysis did not raise any concernf or bias.
