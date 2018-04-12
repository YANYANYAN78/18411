# 18411
100-1
题目：有四个数字：1、2、3、4，能组成多少个互不相同且无重复数字的三位数？各是多少？



#! usr/bin/env python
# -*- coding:UTF-8  -*-


for x in range(1,5):
    for y in range(1,5):
        for z in range(1,5):
            if (x!=y) and (y!=z) and (z!=x):
                print x,y,z


#完善一下总数计数问题
d=[]
for x in range(1,5):
    for y in range(1,5):
        for z in range(1,5):
            if (x!=y) and (y!=z) and (z!=x):
                d.append([x,y,z])
print("一共是%d个"%len(d))
print(d)



#FOR + IF 一行代码处理
list_dad=[1,2,3,4]
list_sun=[a*100+b*10+c for a in list_dad for b in list_dad for c in list_dad if (a!=b and b!=c and c!=a)]
print (list_sun)
print ('total:',len(list_sun))



