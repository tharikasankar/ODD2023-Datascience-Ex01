# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

#  CODE :
# for Data_Set:
```
import pandas as pd
df=pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```
# for Loan_data:
```
import pandas as pd
df=pd.read_csv("/Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```
# Output :
# for Data_Set:
# Data:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/f10ef7e7-de32-4973-affd-42d66307a3c8)

# NON NULL  BEFORE: 
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/1056f2fd-3ead-43f2-9cad-47e6e68bcffe)
# MODE:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/cd173bf5-a277-4b17-b4aa-3a09b1e59e1c)
# MEAN:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/ac6aabc6-f598-4fec-82e2-8306f2687578)
# MEDIAN:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/6be70603-c226-45cb-901f-ed35efe4b5c6)
# NON NULL AFTER:
# Df info:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/b6a99ce9-7e4e-4a3a-bc73-4c1da67d603c)
# Df isnull().sum():
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/a98ab331-3ffd-499d-b30d-7d6aa2e959ba)
# for Loan_Data:
# Data:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/361e0bd1-0299-4d0e-af99-5662dd958d95)
# NON NULL BEFORE:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/632a7d09-eff3-4099-a062-876f40344b8f)
# MODE:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/9126d22e-d9e3-419d-8f81-d57321b3ce06)
# MEAN:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/7e0ea030-e7a3-4388-9f77-a84d6a888b85)
# MEDIEAN:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/bf3081be-9058-40ab-99c6-3c926a891683)
# NON NULL AFTER:
# DF INFO:
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/f36dcdd3-68ff-4f63-a8a2-2dd9f1a7100a)
# DF ISNULL().SUM():
![image](https://github.com/tharikasankar/ODD2023-Datascience-Ex01/assets/119475507/7410797d-6bd8-4db1-ad55-421a280f4292)

# RESULT:
Thus,the given data is read,cleared and the cleaned data is saved into the file.





