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
            <<include your coding and its corressponding output screen shots here>>
            import pandas as pd 
            
data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

print(data)
            <img width="621" height="681" alt="Screenshot 2025-10-04 083135" src="https://github.com/user-attachments/assets/21f0d9e4-e20d-4369-ab91-bd52cde89bc4" />

            import pandas as pd 
            
data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

print(df.isnull())

<img width="672" height="477" alt="Screenshot 2025-10-04 083536" src="https://github.com/user-attachments/assets/83f79e37-0e68-45ac-8ba7-503e695feac1" />

import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

print(df.isnull().sum())

<img width="263" height="175" alt="Screenshot 2025-10-04 083701" src="https://github.com/user-attachments/assets/07f4555d-f892-4838-aeb2-efd43ecd2b11" />

import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

print(df)

df.info

<img width="777" height="701" alt="Screenshot 2025-10-04 083921" src="https://github.com/user-attachments/assets/96655e09-f315-4eac-8ec0-5c2f9f7e46c9" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.dropna()

print("After Dropna")

print(dfd)

<img width="655" height="704" alt="image" src="https://github.com/user-attachments/assets/b92efc2b-c4a3-42d0-84e4-84c54fe7328e" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.dropna(axis=1)

print("After Dropna")

print(dfd)

<img width="477" height="266" alt="image" src="https://github.com/user-attachments/assets/9a2250a7-7753-4210-a064-9682a1118c59" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

df1=df.iloc[[1,3,5],[1,3]]

print(df1)

<img width="321" height="83" alt="image" src="https://github.com/user-attachments/assets/8e63e402-a633-4ea7-9728-7cb2280a25d2" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.dropna(axis=0)

print(df)

print("After Dropna")

print(dfd)

<img width="612" height="714" alt="image" src="https://github.com/user-attachments/assets/f9ba5a9c-ca6d-4861-884d-e97646d333fa" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

print(df.isnull().any())

<img width="320" height="190" alt="image" src="https://github.com/user-attachments/assets/174c0bec-97e9-4245-8e39-35e8ae78e5fa" />


import pandas as pd

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna(0)

print("After FILLNA")

print(dfd)

<img width="754" height="709" alt="image" src="https://github.com/user-attachments/assets/8c43322b-203a-4c9d-a570-9dd8c9746720" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna(method="bfill")

print("After FILLNA")

print(dfd)

<img width="912" height="687" alt="image" src="https://github.com/user-attachments/assets/90499165-53ac-4e4f-a194-540b74be3f4c" />


import pandas as pd

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna({'show_name':'abc','aired
               _on':'monday','original_network':'jio','rating':8.2})
               
print("After FILLNA")

print(dfd)

<img width="731" height="708" alt="Screenshot 2025-10-04 090531" src="https://github.com/user-attachments/assets/0338067d-73fb-42c1-bc93-48a71c3e2d66" 


            import pandas as pd 
            
data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna(df.mean(),inplace=True)

print(df)

print("After FILLNA")

print(dfd)

<img width="722" height="724" alt="image" src="https://github.com/user-attachments/assets/b0694af6-8b6f-4998-8b14-b0235cf74a22" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna(df.mean(),inplace=False)

print("After FILLNA")

print(dfd)

<img width="812" height="712" alt="image" src="https://github.com/user-attachments/assets/9ad60606-06a6-4ce7-ae3e-45de8bd7ddb3" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna(df.mean(),inplace=False)

print("After FILLNA")

print(dfd)

<img width="714" height="708" alt="image" src="https://github.com/user-attachments/assets/181a0e38-5712-4bd9-9c87-a9bf00066040" />


import pandas as pd 

data=pd.read_csv(r"C:\Users\acer\Downloads\Data_set.csv")

df=pd.DataFrame(data)

dfd=df.fillna(df.median(),inplace=False)

print("After FILLNA")

print(dfd)

<img width="793" height="709" alt="image" src="https://github.com/user-attachments/assets/447e6c96-de7a-498a-a311-98768a7bea2c" />


import pandas as pd

import matplotlib.pyplot as plt

import numpy as np

data=pd.read_csv("iris.csv")

print(data)

df=pd.DataFrame(data)

print(pd)

x=df["petal_length"]

y=df["sepal_length"]

plt.bar(x,y)

plt.show()

<img width="757" height="684" alt="image" src="https://github.com/user-attachments/assets/4580a4eb-f3b2-4d18-a526-3530a1c27101" />


import pandas as pd

import matplotlib.pyplot as plt

import numpy as np

data=pd.read_csv("iris.csv")

print(data)

df=pd.DataFrame(data)

print(pd)

x=df["petal_length"]

y=df["sepal_length"]

plt.scatter(x,y)

plt.show()

<img width="772" height="692" alt="image" src="https://github.com/user-attachments/assets/c5150576-6d65-4242-8999-aa6086ffa003" />


import pandas as pd

import matplotlib.pyplot as plt

import numpy as np

data=pd.read_csv("iris.csv")

print(data)

df=pd.DataFrame(data)

print(pd)

dff=plt.boxplot(x="petal_width",data=df)

print(dff)

<img width="1064" height="766" alt="image" src="https://github.com/user-attachments/assets/e055c3ac-2056-4146-be88-3f31c406a7a5" />


import pandas as pd

import matplotlib.pyplot as plt

import numpy as np

data=pd.read_csv("iris.csv")

print(data)

df=pd.DataFrame(data)

print(pd)

x=df["petal_length"]

y=df["sepal_length"]

plt.plot(x,y)

plt.show()

<img width="765" height="689" alt="image" src="https://github.com/user-attachments/assets/456bd290-412f-4b0d-8089-5cc6373e2e2b" />


import pandas as pd

import numpy as np

from scipy import stats

data=pd.read_csv("iris.csv")

df=pd.DataFrame(data)

z_scores = np.abs(stats.zscore(df.select_dtypes(include=[np.number])))

df_cleaned=df[(z_scores<3).all(axis=1)]

df_cleaned

<img width="472" height="373" alt="image" src="https://github.com/user-attachments/assets/4a70a26f-53a8-4eb5-bdaa-677117914420" />


import pandas as pd 

import numpy as np

data_set = pd.read_csv("iris.csv")

df = pd.DataFrame(data_set)

Q1 = df["sepal_width"].quantile(0.25)

Q3 = df["sepal_width"].quantile(0.75)

IQR = Q3 - Q1

lower_bound = Q1 - 1.5 * IQR

upper_bound = Q3 + 1.5 * IQR

print("The Orginal DataSet"
)
print(df)

outliers = df[(df['sepal_width'] < lower_bound) | (df['sepal_width'] > upper_bound)]

print("The Outliers")

print(outliers)<img width="696" height="622" alt="image" src="https://github.com/user-attachments/assets/09260c64-36ec-4014-b5cb-7fa9d42aa9c9" />


df_clean = df[(df['sepal_width'] >= lower_bound) & (df['sepal_width'] <= upper_bound)]

print("The Dataset after removing the outliers")

print(df_clean)

<img width="696" height="622" alt="image" src="https://github.com/user-attachments/assets/b4d527b3-ea3c-43d8-bb96-6b70a793119a" />







                   
                   




















# Result
          <<include your Result here>>
