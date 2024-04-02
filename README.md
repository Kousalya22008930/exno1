# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
df.head(5)
![311437803-e5ee2149-73f3-49b5-afb5-02ce88b26f8a](https://github.com/Kousalya22008930/exno1/assets/119389108/43e4f566-c078-4ccb-999e-1ff134ea79bd)

df.tail(3)
![311437893-a3f27304-586b-4d9e-b349-f37a6c8b0b8b](https://github.com/Kousalya22008930/exno1/assets/119389108/cceeebeb-fccb-4d07-8b0c-7cf74b2a6fdd)

df.info()
![311437993-dbb6ddd0-38ff-469b-9136-bfb622cee6cb](https://github.com/Kousalya22008930/exno1/assets/119389108/3d535d13-2a54-4052-a5c9-83c691a57283)

df.describe()
![311438068-aa9cf5df-ed12-40f4-a0a0-2a9ac7e4d10b](https://github.com/Kousalya22008930/exno1/assets/119389108/06d9a3e0-0187-4f37-9165-bd94dd7759a7)

df.isnull()
![311438100-df6323ee-fbb5-4183-80ff-c7cc04bff548](https://github.com/Kousalya22008930/exno1/assets/119389108/68d87892-9ecd-4be3-bfbf-434cd36734fc)

df.dropna(axis=1)
#df.dropna(axis=0)
![311438179-4eebd25c-b2be-4ba4-8ece-a62928bfd038](https://github.com/Kousalya22008930/exno1/assets/119389108/03f1ee66-7e73-4b7e-95a5-e31f7a040d94)

df.fillna(method='bfill')
#df.fillna(method='ffill')
![311438239-ea314ab4-1af3-4fdb-b99e-c2c493cdb5f1](https://github.com/Kousalya22008930/exno1/assets/119389108/c2621f52-1027-40af-96da-9131968f8a93)

import seaborn as sns
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
![311438367-1a89a3a4-6ea1-46f2-aae8-8dfd5822dd2f](https://github.com/Kousalya22008930/exno1/assets/119389108/d9e665db-6997-4fc0-9418-ff3287af41ea)

df.dropna(inplace=True)
sns.heatmap(df.isnull(),yticklabels=False,annot=True)
![311438410-d12ac9ef-219f-426b-b8fd-bc0b9308284b](https://github.com/Kousalya22008930/exno1/assets/119389108/8618d15f-7378-4e70-93e1-1cb43aa84f13)

import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
df=pd.read_csv("heights.csv")
df
![311438458-8feaca32-efb6-4a23-a1ee-4607d6628f1c](https://github.com/Kousalya22008930/exno1/assets/119389108/811718a1-c88e-484a-9565-d0bd2a9047b9)

sns.boxplot(data=df)
![311438501-a64b5776-827b-4e0d-be1b-87ebcabaa16c](https://github.com/Kousalya22008930/exno1/assets/119389108/4efae272-6aa4-48e1-bd4d-eee073d8348b)

sns.scatterplot(data=df)
![311438537-87961d5e-d834-4fd9-a6a3-5bd5ce5f7d81](https://github.com/Kousalya22008930/exno1/assets/119389108/b167e468-e255-4332-804b-d5e7eba0ad28)

qm=df[((df['height']>=low)&(df['height']<=high))]
qm
![311438601-66477c7f-9d10-4566-a7a6-8c8d0d00b9a0](https://github.com/Kousalya22008930/exno1/assets/119389108/c52e62ae-50b0-43f5-88a5-554e53bfea88)

sns.boxplot(data=qm)
![311438675-0dd34661-bb72-4aea-95c0-f7d3dfcfaa43](https://github.com/Kousalya22008930/exno1/assets/119389108/03d93be2-ff1f-4bb0-9484-2cbd29d452e4)

sns.scatterplot(data=qm)
![311438725-0941b0c5-8093-425c-b219-39b0a3fed0fa](https://github.com/Kousalya22008930/exno1/assets/119389108/04fd7a27-dd8c-481a-b368-80a152b41e71)
```
## RESULT:
Cleaning of Data and Removing of Outline executed successfully.
