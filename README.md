# split_formula
材料化学式的正则表达式操作

参见 split_formula.ipynb

```
def split_formula(s):

    t = re.findall(r'[\d+<\.\d+>?]+|[a-zA-Z]+',s)
    
    return(t)
```

案例1：data = pd.DataFrame([['James', 'FA0.2MA0.7APA0.1Pb0.8Sn0.2Cl0.9F1.1I1'],['Sam', ' CH3NH3PbI3'], ['Billy', '(CH3NH3)PbI3'], ['Sarah', '(CH5N2)SnI3'], ['Felix', 'MAPbBr3']], columns=['Name', 'formula'])

案列2：Formular1 = "FA0.2MA0.7APA0.1Pb0.8Sn0.2Cl0.9F1.1I1"

```
import pandas as pd
import re
import numpy as np
data = pd.DataFrame([['James', 'FA0.2MA0.7APA0.1Pb0.8Sn0.2Cl0.9F1.1I1'],['Sam', ' CH3NH3PbI3'], ['Billy', '(CH3NH3)PbI3'], ['Sarah', '(CH5N2)SnI3'], ['Felix', 'MAPbBr3']], columns=['Name', 'formula'])
Formular1 = "FA0.2MA0.7APA0.1Pb0.8Sn0.2Cl0.9F1.1I1"
split_formula(Formular1)
pd.set_option('display.max_colwidth', 900)
data['split'] = data['formula'].apply(split_formula)
data
```

```
def split_formula_test0(s):
    t = re.findall(r'[\d+<\.\d+>?]+|[a-zA-Z]+',s)
    u = pd.DataFrame(t)   
    v = u.T   
    return(v)
```

```
def split_formula_test1_2Dwrong(s):
    t = re.findall(r'[\d+<\.\d+>?]+|[a-zA-Z]+',s)   
    u = pd.DataFrame(t)   
    v = u.T
    display(v)
```
