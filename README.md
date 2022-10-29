# split_formula
材料化学式的正则表达式操作


def split_formula(s):

    t = re.findall(r'[\d+<\.\d+>?]+|[a-zA-Z]+',s)
    
    u = pd.DataFrame(t)
    
    v = u.T
    
    display(v)

Formular1 = "FA0.2MA0.7APA0.1Pb0.8Sn0.2Cl0.9F1.1I1"

split_formula(Formular1)

