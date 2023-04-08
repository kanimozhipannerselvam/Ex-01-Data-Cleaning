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

import pandas as pd

df=pd.read_csv("/content/Data_set.csv")

print(df)

df.head(5)

df.info()

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

# OUPUT

![image](https://user-images.githubusercontent.com/119476060/230703417-3e225316-81ce-43aa-ba38-7013515b8b0f.png)

![image](https://user-images.githubusercontent.com/119476060/230703419-1f8322c4-1af4-45b2-a7e8-982d74b1f9de.png)

![image](https://user-images.githubusercontent.com/119476060/230703425-4d758aac-f2e9-486e-b868-dfb99030a3bb.png)

![image](https://user-images.githubusercontent.com/119476060/230703429-f9538a16-025a-4436-ac57-5a3ce40847a6.png)

![image](https://user-images.githubusercontent.com/119476060/230703430-54306121-cd0e-4f97-b092-d32ad9c3f9d3.png)

![image](https://user-images.githubusercontent.com/119476060/230703434-a19bdcff-ce5b-4df0-a61a-4f3c5741724d.png)

![image](https://user-images.githubusercontent.com/119476060/230703439-70fd7839-ab45-4ca1-930b-d64a8ae0a312.png)

![image](https://user-images.githubusercontent.com/119476060/230703444-dc7b6ded-6a26-465b-9c98-81c5e0ec57b4.png)

#RESULT

Hence the given data is read and perform data cleaning and save the cleaned data to a file.






