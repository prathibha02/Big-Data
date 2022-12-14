# Big-Data
## Background

In this assignment, we will put your ETL skills to the test. Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines. One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer. Our first goal for this assignment will be to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. The second goal will be to use PySpark or SQL to perform a statistical analysis of selected data.

1. Create DataFrames to match production-ready tables from two big Amazon customer review datasets.

2. Analyze whether reviews from Amazon's Vine program are trustworthy.


### Level 1

* We use the provided schema to create tables in the RDS database.

* We create two separate Google Colab notebooks and **extract** any two datasets from the list at [review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt). Put each dataset into its own notebook.


* We complete the following steps for each notebook (one dataset per notebook).

  * Count the number of records (rows) in the dataset.

  * Transform the dataset to fit the tables in the [schema file](../Resources/schema.sql). Be sure that the DataFrames match in data type and in column name.

  * Load the DataFrames that correspond to tables into an RDS instance. 

### Level 2

In Amazon's Vine program, reviewers receive free products in exchange for reviews.

  ![vine01.png](../Images/vine01.png)

Amazon has several policies to reduce the bias of its Vine reviews: [https://www.amazon.com/gp/vine/help?ie=UTF8](https://www.amazon.com/gp/vine/help?ie=UTF8).

But are Vine reviews truly trustworthy? Our task is to investigate whether Vine reviews are free of bias. We can use either PySpark or, for an extra challenge, SQL to analyze the data.

* If we choose SQL, first use Spark on Colab to extract and transform the data and then load it into a SQL table on your RDS account. Perform your analysis with SQL queries on RDS.

* While there are no strict requirements for the analysis, consider steps you can take to reduce noisy data, such as filtering for reviews that meet a certain number of helpful votes, total votes, or both.

* We submit a summary of your findings and analysis.