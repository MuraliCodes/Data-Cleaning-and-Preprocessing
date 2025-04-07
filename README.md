# Data Cleaning & Preprocessing

This project showcases data cleaning and preprocessing techniques using Python ('pandas', 'numpy') on a marketing campaign dataset.


## Dataset

The dataset ('marketing_campaign.csv') contains **2240 records** and **29 columns**, covering:
-Customer demographics (e.g., age, marital status, education)
-Product spending
-Campaign responses


## Tools & Libraries
-Python 3.x
-Pandas
-Numpy

## Data Cleaning & Preprocessing Steps

1.Load Dataset --python
df=pd.read_csv("marketing_campaign.csv",sep='\t')

2.Missing Values
•	Imputed missing Income values with the column mean.

3.Data Conversion
•	Converted Dt_customer column to datetime format.

4.Feature Engineering
•	Created new features
Age from Year_Birth
Total_Children from Kidhome + Teenhome
Total_Spend from all product-related spending columns

  5.Categorical Cleaning
•	Standardized Education and Marital_Status fields by unifying inconsistent values.

6.Column Dropping
•	Removed Z_CostContact, Z_Revenue, and ID as they were constant or unnecessary.


##  Before vs After Cleaning (Example)

| Column         | Raw Value            | Cleaned Value         |
|----------------|----------------------|------------------------|
| Marital_Status | "YOLO"               | "Single"              |
| Education      | "2n Cycle"           | "Master"              |
| Income         | NaN                  | 52247.25 (mean filled)|
