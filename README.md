拉数据
import pymysql
import pandas as pd
import numpy as np
import re
conn=pymysql.connect(host='',
                     user='',
                     password='',
                     database='',
                     port=,
                     charset='')
aa=pd.read_sql("",con=conn)
上句中引号内填sql代码，不能换行

清洗
aa=pd.read_csv("d:/bloodtest.csv")
aa1=aa.replace({'MW':0,'UW':0,'M':1})
aa2=aa1.replace("[^0-9.]","",regex=True)
aa3 = aa2.convert_objects(convert_numeric=True)
