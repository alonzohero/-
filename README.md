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


待处理问题：
1.正则替换完成后，要先处理异常值再填空值，处理异常值的方法可以用最大值跟均值或75分位值进行比较，循环删除。但是有nan是否会影响describe的计算？
2.
