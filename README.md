# AIM:
To read a given dataset and remove outliers and save a new dataframe.

# ALGORITHM:
(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them

# PROGRAM:
```python3
import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

df = pd.read_csv("/content/heights.csv")

sns.boxplot(data=df)

sns.scatterplot(data=df)

max =df['height'].quantile(0.90)

min =df['height'].quantile(0.15)

max

min

dq = df[((df['height']>=min)&(df['height']<=max))]

dq

low = min-1.5*iqr

high = max+1.5*iqr

dq = df[((df['height']>=min)&(df['height']<=max))]

 dq

## ZSCORE:

 import pandas as pd

import numpy as np

import seaborn as sns

import pandas as pd

from scipy import stats

data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}

df = pd.DataFrame(data)

df

sns.boxplot(data=df)

z = np.abs(stats.zscore(df))

print(df[z['weight']>3])

val = [12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]

out=[]

def d_o(val):

  ts=3
  
  m=np.mean(val)
  
  sd=np.std(val)
  
  for i in val:
  
    z=(i-m)/sd
    
    if np.abs(z)>ts:
    
      out.append(i)
      
  return out

  op = d_o(val)

  op 
```
  # OUTPUT:
![1](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/a2932bd6-aa46-48e2-b461-604efeb2656e)
![2](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/64ec2090-16ce-4617-80c3-96284e4cc8f3)
![3](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/48840d85-b207-42bc-a817-d044b745948a)
![4](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/15e7b7e4-a9de-4a87-ac20-7da7553a7317)
![5](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/6f99d4b8-29b3-42a5-bd99-8673c1925652)
![6](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/845f2c77-6272-4fc9-896c-759cade8639c)
![7](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/cab7b9e9-81d2-44e0-a48c-e13520cd493e)
![8](https://github.com/Krupa-Varsha-P/DS-EX-2/assets/100466625/0227b70d-f451-41e9-b4f0-094ab1dc027a)

# RESULT:
  Thus, the given data is read,remove outliers and save a new dataframe was created and executed successfully.
