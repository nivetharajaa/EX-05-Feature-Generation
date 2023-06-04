# EX-05-Feature-Generation


# AIM

To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM

### STEP 1

Read the given Data

### STEP 2

Clean the Data Set using Data Cleaning Process

### STEP 3

Apply Feature Generation techniques to all the feature of the data set

### STEP 4

Save the data to the file


# CODE

# data.csv

import pandas as pd

import seaborn as sbn

df=pd.read_csv("/content/data.csv")

df.info()

df.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

df['Ord_2'] = le.fit_transform(df['Ord_2'])

sbn.set(style ="darkgrid")

sbn.countplot(df['Ord_2'])from sklearn.preprocessing import OneHotEncoder

enc = OneHotEncoder()

enc = enc.fit_transform(df[['City']]).toarray()

encoded_colm = pd.DataFrame(enc)

df = pd.concat([df, encoded_colm], axis=1)

df = df.drop(['City'], axis=1)

df.head(10)

df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2'])

df.head(10)

df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1'])

df.head(10)

# encoding.csv
import pandas as pd

import seaborn as sbn

data=pd.read_csv("/content/Encoding Data.csv")

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

data['ord_2'] = le.fit_transform(data['ord_2'])

sbn.set(style ="darkgrid")

sbn.countplot(data['ord_2'])

from sklearn.preprocessing import OneHotEncoder

en = OneHotEncoder()

en = en.fit_transform(data[['nom_0']]).toarray()

encoded_colm = pd.DataFrame(en)

data= pd.concat([data, encoded_colm], axis=1)

data= data.drop(['nom_0'], axis=1)

data.head(10)

data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2'])

data.head(10)

 # titanic.csv
 
 import pandas as pd
 
import seaborn as sbn

dt=pd.read_csv("/content/titanic_dataset.csv")

dt.info()

dt.isnull().sum()

dt['Age']=dt['Age'] . fillna(dt ['Age'].mean())

dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0])

dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0])

dt.isnull().sum( )

from sklearn.preprocessing import LabelEncoder

lc = LabelEncoder()

df['Sex'] = lc.fit_transform(df['Sex'])

sbn.set(style ="darkgrid")

sbn.countplot(df['Sex'])

from sklearn.preprocessing import OneHotEncoder


enc= OneHotEncoder()

enc= enc.fit_transform(dt[['Name']]).toarray()

encoded_colm = pd.DataFrame(enc)

dt= pd.concat([dt, encoded_colm], axis=1)

dt= dt.drop(['Name'], axis=1)

dt.head(10)

dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket'])

df.head(10)

dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked'])

df.head(10)

# OUPUT

## Data.csv


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/29f4af59-6558-40df-97cd-d59b46d5f674)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/ed57fc28-cb7d-4f8d-b0cb-c9ab82073262)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/1a1c258a-4495-449a-85e3-974aef2e44a2)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/949c602f-f6ba-4756-8bac-bfbcae748ba3)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/3e3ee1a4-4af2-461c-bcba-c54b94127c07)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/b3cf028b-b0c9-494b-add6-e59beeb7555d)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/d979d9c9-4063-4231-8b22-4250a1bf988a)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/f96e8125-9360-48eb-ba5c-2cfb86761362)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/bff106ae-52d6-4c68-ac17-5da71cb84850)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/7a2f66fd-95fb-4a1c-85c2-70c13b938d54)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/edfa721e-3717-4acf-854a-772a8ad7f66b)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/dfcd480d-13ea-4cfa-93e6-0d543ddcaef2)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/773db1f9-ca11-45e3-895e-e93a98398609)


![image](https://github.com/nivetharajaa/EX-05-Feature-Generation/assets/120543388/b6e01123-0ad4-4020-be12-6520d02145cd)


# RESULT

The Feature Generation process was performed and saved the data to a file.


