# 18411
100-1
题目：有四个数字：1、2、3、4，能组成多少个互不相同且无重复数字的三位数？各是多少？



#! usr/bin/env python
# -*- coding:utf-8  -*-


for x in rang(1,5):
    for y in rang(1,5):
        for z in rang(1,5):
            if (x!=y) and (y!=z) and (z!=x):
                print x,y,z
