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
# Output :
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



