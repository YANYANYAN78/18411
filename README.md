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




#用数做元素，区间最大最小值理念
list=[]
for n in range(123,433): #一定要是433因为range特殊写432会取不到432本身
    z=n%10  #除以10取余数得到个位数字
    y=(n%100)//10   #%100除以100取余数//10除以10取整数，这样就拿到了十位上的数字
    x=(n%1000)//100
    if z!=y and y!=x and x!=z and 0<z<5 and 0<x<5 and 0<y<5:
        list.append(n)   #符号是小括号且对象是n
        
print ('total is:',len(list))   #不要忘了加逗号和单引号
print (list)









