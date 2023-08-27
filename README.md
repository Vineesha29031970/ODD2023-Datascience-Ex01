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

# CODE and OUTPUT
import pandas as pd


df=pd.read_csv("/content/SAMPLEDS - Sheet1.csv")

df
<img width="407" alt="exp1 ds" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/cb3f4d31-3221-4bcc-b4e3-3ff3c8f38748">


df.head
<img width="665" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/1a0d4049-5868-43f0-97e1-5ea137e3c9ba">

<img width="165" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/07edb2be-1eea-41be-a480-2914d61516f3">

df.tail
<img width="821" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/c8809bd2-b919-41eb-9542-ed4855582e72">

<img width="169" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/7c84c010-dfe2-414c-9fed-d359584ad63e">

df.shape
<img width="88" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/ab9e6a2b-c5c1-427c-a3c1-d563b20fe96c">

df.describe
<img width="673" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/a277a1ed-cd27-43b1-9420-bb8f777d37f9">


<img width="168" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/0a5633d0-1471-4c3d-8134-37662024ccaf">


df.info

<img width="683" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/7ab9c669-961d-4aba-99d8-e2ce3aed82fa">


<img width="164" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/fd590d18-137f-4794-a365-46aac0991890">

df.isnull().sum()


<img width="140" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/1ae4af0b-b4cb-47c3-b1ee-8fbb021bc81f">


df.dropna(how='any').shape


<img width="88" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/7dd36104-2336-4108-9336-a65216f47947">


x=df.dropna(how='any')

df


<img width="404" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/8cf8478c-1731-4850-a665-b240a8e0d64c">


df.dropna(how='all').shape


<img width="57" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/c8048cef-8c20-4245-a3e7-2d7af6bc0d0a">


df

<img width="412" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/2dc6de73-860c-4ff2-9987-fe483e699ae1">


tot=df.dropna(subset=['TOTAL'],how='any')

tot

<img width="428" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/7eb44b4c-959d-4c0e-80e8-6ab6f865b71b">


tot=df.dropna(subset=['M1','M2','M3','M4'],how='any')


tot


<img width="428" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/04b2fd68-e1c4-4985-a10f-f2a095ed0f43">


df.fillna(0)


<img width="419" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/8f4ca1d7-b622-4aa5-88ae-6f2c3e82fd76">


df

<img width="430" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/eef65866-a09c-4f9d-a2fe-4fcab70cd11d">


df.fillna(method='ffill')


<img width="458" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/f9f865df-ef4c-4927-95f2-fa47d5fc9ec3">


df.fillna(method='bfill')


<img width="428" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/2af6eb00-8c56-47ab-9dd7-c4746f9a6d07">


df.interpolate()


<img width="432" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/6db6a18e-fce0-4dc1-b835-92122e57e7f8">


mn=df.TOTAL.mean()

mn

<img width="42" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/594b851a-068f-4753-a9c1-94611a92ea57">


df.TOTAL.fillna(mn,inplace=True)

df


<img width="458" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/62099fc6-836f-46e1-a538-c8c68037b0b3">


l=df.M1.interpolate()

l


<img width="123" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/9b332a08-1ae5-458c-bf0f-05aa5b9dae38">


df.M1.fillna(l,inplace=True)

df


<img width="493" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/1daabc8c-a6e2-4969-aa99-8ea22c43de9e">


mn=df.TOTAL.median()
mn


<img width="47" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/81eb70a5-660e-4e0e-a652-8e7bf78591ef">


mn=df.TOTAL.mode()
mn

<img width="179" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/d17ee05d-77e7-4cf7-9695-d366326b213b">


df.isnull()


<img width="359" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/342a2653-e50e-44b1-894c-f2eccfd9c395">


df.duplicated()


<img width="91" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/96320f8f-d7f9-41eb-9aad-ae9a636ccf69">


df.drop_duplicates(inplace=True)

df


<img width="419" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/a21a19dd-c107-47f7-89bd-ad0c4fb4a903">


df['cd']=pd.to_datetime(df['DOB'])

df


<img width="508" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/7a04218d-68cf-4411-80a6-9a5725a4d63d">


for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)

df


<img width="503" alt="image" src="https://github.com/Vineesha29031970/ODD2023-Datascience-Ex01/assets/133136880/85a7d5e8-22dd-446c-8545-275efd247c54">



