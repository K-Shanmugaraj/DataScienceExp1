# Ex. 1 Data Cleaning and Outlier Detection & Removal

## AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

## Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is
incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about
erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the
information.
## ALGORITHM:
STEP 1<br>
Read the given Data<br>
STEP 2<br>
Get the information about the data<br>
STEP 3<br>
Remove the null values from the data<br>
STEP 4<br>
Save the Clean data to the file<br>
STEP 5<br>
Remove outliers using IQR<br>
STEP 6<br>
Use zscore of to remove outliers<br>
## PROGRAM:
DEVELOPED BY : SHANMUGA RAJ.K
REG NO : 212223040192
### Client:
```
import pandas as pd
data=pd.read_csv("/content/SAMPLEIDS.csv")
data
```
![Screenshot 2025-03-04 102727](https://github.com/user-attachments/assets/8c258a9d-6196-48f2-baad-83a832345213)
```
data.head(5)
```
![Screenshot 2025-03-04 102738](https://github.com/user-attachments/assets/a9f92709-e8a5-4b78-815f-b1e800834eb1)
```
data.tail(5)
```
![Screenshot 2025-03-04 102746](https://github.com/user-attachments/assets/688fe387-de29-4e46-aab3-fe0a598112cf)
```
data.isnull().sum()
```
![Screenshot 2025-03-04 102806](https://github.com/user-attachments/assets/9413a0cf-9a69-485e-94c1-60c3b330f6c6)
```
data.isnull().any()
```
![Screenshot 2025-03-04 102813](https://github.com/user-attachments/assets/84439138-1928-4427-a74c-1ed9d53bcf0a)
```
data.dropna()
```
![Screenshot 2025-03-04 102824](https://github.com/user-attachments/assets/a5c1eca6-9a35-4d12-a0e1-e4fcd82a58f0)
```
data.fillna(0)
```
![Screenshot 2025-03-04 102836](https://github.com/user-attachments/assets/e6a44033-3f79-435e-812d-a3765579156e)
```
data.fillna(method = 'ffill')
```
![Screenshot 2025-03-04 102851](https://github.com/user-attachments/assets/e2e050ea-164a-4dcf-ba9d-f8a0e3a5ca71)
```
data.fillna(method = 'bfill')
```
![Screenshot 2025-03-04 102902](https://github.com/user-attachments/assets/7e77692e-2efb-4782-9ac3-972f383eab47)
```
data_dropped = data.dropna()
data_dropped
```
![Screenshot 2025-03-04 102912](https://github.com/user-attachments/assets/5c4f8e44-ac08-4ab2-8213-6ccf1e9f9bbc)
```
data.fillna({'GENDER':'MALE','NAME':'SRI','ADDRESS':'POONAMALEE','M1':98,'M2':87,'M3':76,'M4':92,'TOTAL':305,'AVG':89.999999})
```
![Screenshot 2025-03-04 102925](https://github.com/user-attachments/assets/b0dbd700-e932-4af0-9e58-0c6907d1514e)


