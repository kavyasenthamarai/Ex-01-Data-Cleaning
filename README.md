# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)

df.head(5)

df.tail(5)

df.describe()

df.info()

df.isnull().sum()

df=df[~df.duplicated()]
print(df)

df['Gender'].fillna(value=df['Gender'].mode())

df['LoanAmount'].fillna(value=df['LoanAmount'].median())
```
# OUPUT
![ds ex1](https://user-im![ds ex 2](https://user-images.githubusercontent.com/118668727/226526489-76314263-c2be-41f9-ae28-71b82f2e4514.png)
![ds ex 2](https://user-images.githubusercontent.com/118668727/226526529-2ba5efbf-59ea-4532-aa27-de7ed8a16ed6.png)
![ds ex 3](https://user-images.githubusercontent.com/118668727/226526541-47e5ec2f-7faf-40ce-bde7-c68ef6261e6e.png)
![ds ex 4](https://user-images.githubusercontent.com/118668727/226526563-682984d0-7cb3-4f43-b868-5b3bfeddc0f2.png)



