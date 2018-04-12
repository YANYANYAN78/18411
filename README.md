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
for x in range(1,5): #一层层加上约束条件
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




#逐个技术+=1

num=[1,2,3,4]
i=0
for x in num:
    for y in num:
        for z in num:
            if x!=y and y!=z and z!=x:
                i+=1
                print (x,y,z) #注意加逗号
print ('total is:',i)




#去除重复  
list_dad=['1','2','3','4']
list_sun=[]
for x in list_dad:
    for y in list_dad:
        for z in list_dad:
            if len(set(x+y+z))==3:#去除重复元素
                list_sun+=[int(x+y+z)]  #注意这种形式的列表增加元素和append（i）的不同
                              
print ('tatal is:',len(list_sun))
print(list_sun)


#类似概率算法-数学
list = [1,2,3,4]
for i in list:
    list1 = list.copy()
    list1.remove(i)
    for j in list1:
        list2 = list1.copy()
        list2.remove(j)
        for k in list2:
            print(i, j, k)
