# Mini-Project
EXPLORATORY DATA ANALYSIS OF ALCOHOL CONSUMPTION
# AIM 
To implement the exploratory data analysis of alcohol consumption .
# ALGORITHM

### STEP 1:

Collect the dataset from required website.

### STEP 2:

Import dataset in the google colab.

### STEP 3:

Import all the libraries.

### STEP 4:

Detect the outlier and plot the graph.

### STEP 5:

Remove the outliers.

### STEP 6:

Standardize the analyzation by using Zscore.

### STEP 7:

Run the program.

# PROGRAM

Developed by:V.DHARSHAN

Reg no :2222230031

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/student-mat.csv")
df
df.head()
df.info()
df.isnull().sum()
df.describe
df.shape
sns.boxplot(data=df)
df.drop('age',axis=1)
sns.boxplot(x='age',data=df)
q1 = df['age'].quantile(0.35)
q3 = df['age'].quantile(0.65)
print("First Quantile =",q1,"\nSecond Quantile =",q3)
IQR = q3-q1
high = q3+1.5*IQR
low = q1-1.5*IQR
df1 =df[((df['age']>=low)&(df['age']<=high))]
df1
sns.boxplot(x="age",data=df1)
df1.shape
from scipy import stats
import numpy as np
z = np.abs(stats.zscore(df['age']))
df2 = df[(z<3)]
df2
df2.shape
sns.boxplot(x="age0",data=df2)

```
# OUTPUT


![Screenshot 2023-06-16 115929](https://github.com/Dharshan011/Mini-Project/assets/113497491/71d30341-dc62-4bcb-b929-1df0cd98afeb)


![Screenshot 2023-06-16 115938](https://github.com/Dharshan011/Mini-Project/assets/113497491/0c92057b-b8cb-424e-bc5f-8c6249d8c37b)

![Screenshot 2023-06-16 115949](https://github.com/Dharshan011/Mini-Project/assets/113497491/c300fa92-e96b-406e-9d5a-40cdc712f24b)


![Screenshot 2023-06-16 120000](https://github.com/Dharshan011/Mini-Project/assets/113497491/bf1aa7a3-0a1b-49cf-a63a-0292c325405b)

![Screenshot 2023-06-16 120012](https://github.com/Dharshan011/Mini-Project/assets/113497491/466ed54c-6af3-4fbc-a8ea-605119281da0)


![Screenshot 2023-06-16 120018](https://github.com/Dharshan011/Mini-Project/assets/113497491/54a4d370-6dcf-4460-a88a-6f5c509494c6)


![Screenshot 2023-06-16 120031](https://github.com/Dharshan011/Mini-Project/assets/113497491/f41313b6-d7c7-45cd-8aef-186725e20307)



![Screenshot 2023-06-16 120052](https://github.com/Dharshan011/Mini-Project/assets/113497491/dc56acfb-1b68-4182-ad6b-a7140c0be478)

![Screenshot 2023-06-16 120100](https://github.com/Dharshan011/Mini-Project/assets/113497491/0916bc42-14b5-4d77-938e-c3b2e2cd51f9)



![Screenshot 2023-06-16 120105](https://github.com/Dharshan011/Mini-Project/assets/113497491/c3d98e04-0da7-4b10-8193-6bb48cac4b95)





![Screenshot 2023-06-16 120114](https://github.com/Dharshan011/Mini-Project/assets/113497491/fe21c848-a113-47c2-8e3f-90d62c6155da)



![Screenshot 2023-06-16 120121](https://github.com/Dharshan011/Mini-Project/assets/113497491/2e5e67fa-0fe4-46c5-9cdd-d34e16c1d635)



![Screenshot 2023-06-16 120130](https://github.com/Dharshan011/Mini-Project/assets/113497491/c31ebc02-d8c4-4f92-8d53-ba47405ce6dc)


# RESULT

Hence the implementation of data analysis of alcohol consumption is detected successfully.


