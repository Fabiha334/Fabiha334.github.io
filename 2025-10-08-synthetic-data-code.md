layout: post
title: "Synthetic Data Analysis Code"
date: 2025-10-08
categories: [data-science]
tags: [python, pandas, logistic-regression]


---
layout: post
title: "PDF to Markdown: Embedded Code from synthetic_data.pdf"
date: 2025-10-08
categories: [notes]
tags: [jekyll, pdf, code]
---

Below is the raw text extracted from **synthetic_data.pdf**, embedded inside a code block so it renders as *code* in your Jekyll site.  
If you're using **jwillmer/jekyllDecent**, drop this file into your repository's `_posts/` folder.

> Source: synthetic_data.pdf

```
This is your notebook - go crazy
The dataset for you to play with is called:
train.csv
test.csv
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, confusion_matrix
train_data = pd .read_csv("train.csv")
test_data = pd .read_csv("test.csv")
train_data .head( 7)
train_data .info()student_idsexageaddressfamsizemother_educationfather_edu
0 10000M17Paris,
France3 nonesec
ed
1 10001F21Shanghai,
China3secondary
educationhigher ed
2 10002M21Toronto,
Canada4primary educationsec
ed
3 10003M21Paris,
France4 nonesec
ed
4 10004M18Sydney,
Australia4 none5th to 9t
5 10005F21New
York, USA0 none5th to 9t
6 10006M19Tokyo,
Japan4higher educationhigher ed
7 rows × 22 columns
In [2]:
In [3]:
In [4]:
In [5]:
Out[5]:
In [6]:

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 4500 entries, 0 to 4499
Data columns (total 22 columns):
 #   Column                       Non-Null Count  Dtype  
---  ------                       --------------  -----  
 0   student_id                   4500 non-null   int64  
 1   sex                          4500 non-null   object 
 2   age                          4500 non-null   int64  
 3   address                      4500 non-null   object 
 4   famsize                      4500 non-null   int64  
 5   mother_education             4500 non-null   object 
 6   father_education             4500 non-null   object 
 7   Mothers_job                  4500 non-null   object 
 8   Fathers_job                  4500 non-null   object 
 9   traveltime                   4052 non-null   float64
 10  studytime                    4500 non-null   int64  
 11  failures                     4500 non-null   int64  
 12  paid_tutorials               4500 non-null   object 
 13  extra_curricular_activities  4500 non-null   object 
 14  wants_higher_education       4500 non-null   object 
 15  home_internet_access         4500 non-null   object 
 16  romantic_relationship        4500 non-null   object 
 17  freetime_after_school        3732 non-null   float64
 18  alcohol_consumption          4500 non-null   int64  
 19  health                       4500 non-null   int64  
 20  school_absences              4500 non-null   int64  
 21  school_grade_percentage      4500 non-null   int64  
dtypes: float64(2), int64(9), object(11)
memory usage: 773.6+ KB
train_data .shape
(4500, 22)
**this gives us the stats necessary
**
train_data .describe()
In [7]:
Out[7]:
In [8]:

train_data .isnull() .sum()
student_id                       0
sex                              0
age                              0
address                          0
famsize                          0
mother_education                 0
father_education                 0
Mothers_job                      0
Fathers_job                      0
traveltime                     448
studytime                        0
failures                         0
paid_tutorials                   0
extra_curricular_activities      0
wants_higher_education           0
home_internet_access             0
romantic_relationship            0
freetime_after_school          768
alcohol_consumption              0
health                           0
school_absences                  0
school_grade_percentage          0
dtype: int64
train_data["student_id"] .value_counts()student_id agefamsizetraveltimestudytime
count4500.0000004500.0000004500.0000004052.0000004500.000000
mean12492.90444418.5340002.5140002.5217182.509111
std1440.1382222.3053131.713804 1.1157511.117922
min10000.00000015.0000000.0000001.0000001.000000
25%11246.75000017.0000001.0000002.0000002.000000
50%12486.50000019.0000003.0000003.0000002.000000
75%13743.25000021.0000004.0000004.0000004.000000
max14999.00000022.0000005.0000004.0000004.000000
Out[8]:
In [9]:
Out[9]:
In [10]:

student_id
10000    1
10001    1
10002    1
10003    1
10004    1
        ..
14995    1
14996    1
14997    1
14998    1
14999    1
Name: count, Length: 4500, dtype: int64
train_data .tail( 5)
train_data .shape
(4500, 22)
train_data .head( 1)
table_pivot = train_data .pivot_table(index ='romantic_relationship'
                    columns ="sex",
                    values ='school_grade_percentage')
plt .figure(figsize =( 2 0, 2 0))
table_pivot .plot(kind ='bar',student_idsexageaddressfamsizemother_educationfather_
4495 14995M18Paris,
France2secondary
educationprimary
4496 14996F17London,
UK0secondary
education
4497 14997M20Paris,
France3higher educationprimary
4498 14998F20New
York,
USA3secondary
educationhigher
4499 14999F19Toronto,
Canada3primary education
5 rows × 22 columns
student_idsexageaddressfamsizemother_educationfather_edu
0 10000M17Paris,
France3 noneseco
edu
1 rows × 22 columns
Out[10]:
In [11]:
Out[11]:
In [12]:
Out[12]:
In [13]:
Out[13]:
In [14]:
In [16]:

                    stacked =True, # what happens if you make this 
                    color =['lightgreen', 'lightblue'])
plt .title('romantic ', fontsize = 2 0)
plt .xlabel('Pclass', fontsize = 1 5)
plt .ylabel('Count', fontsize = 1 5)
plt .xticks(fontsize = 1 2)
plt .yticks(fontsize = 1 2)
plt .show()
<Figure size 2000x2000 with 0 Axes>
 
In [0]:
```
