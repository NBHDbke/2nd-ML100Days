# 2nd-ML100Days

#!/usr/bin/env python
# coding: utf-8

# #### Homework 1  猜數字

# In[ ]:


import random
ans = random.randint(1, 5)
user = int(input('請猜1到5的一個號碼: '))

if ans == user:
    print('Right, answer is:', ans)
else:
    print('Wrong, answer is:', ans)


# #### Homework 2  印出範圍內的質數

# In[ ]:


import math

m = input('Please enter a number: ')
while m.isdigit() == False:
    m = input('You enter a float, please enter a int: ')
else:
    m = int(m)

a1 = []
for i in range(2, m+1):
    if i <= 3:
        a1.append(i)
    else:
        for j in range(2, int(math.sqrt(i))+1):
            if i%j == 0:
                break
        else:
            a1.append(i)

for i in a1:
    print('%d is prime' % i)


# #### Homework 3  猜數字_終極密碼

# In[ ]:


def validation_int(n):
    if n.isdigit() == True and (1 <= int(n) <= 100):
        return True
    else:
        return False

import random
ans = random.randint(1, 100)
guess = [0]

while guess[-1] != ans:
    a = input('Please enter a int: ')

    while validation_int(a) == False:
        a = input('Out of range, please enter a int between 1~100: ')
        if validation_int(a) == False:
            continue
    else:
        a = int(a)
        guess.append(a)
        if a > ans:
            print('你這次猜%d, 你猜了%d次, 猜錯了，再小一點!' % (a, len(guess)-1))
        elif a < ans:
            print('你這次猜%d, 你猜了%d次, 猜錯了，再大一點!' % (a, len(guess)-1))
        else:
            print('你這次猜%d, 你猜了%d次, 猜對了!' % (a, len(guess)-1))

---------------------------------------
#!/usr/bin/env python
# coding: utf-8

# #### Functions

# In[ ]:


# str()                    字串函數
# int()                    整數函數，無條件捨去
# type()                   查詢屬性函數
# print()                  輸出函數, print(value, ..., sep = ' ', end = '\n'), 輸出預設以空白分隔
# input()                  取得使用者輸入資訊, 輸出為字串, input('Please Enter a Number: ')
# eval()                   可將資料轉成數值型態，前提是，原資料亦為數值型別: int or float
# math.pi                  圓周率
# math.sqrt()              求平方根
# random.randint(min, max) 回傳 [min, max] 之間的亂數
# random.choose(sequence)  回傳 sequence 中的任一數值, sequence可以是range, str, list...etc
# range(star, stop, step)  回傳一個range數列, star ~ stop-1
# list.append()            在list尾端新增一個元素
# list.extend(e1, e2,...)  在list尾端新增多個元素
# list.insert(loca, e1)    在list的loca處, 新增一個元素
# list = list + list       也行，但不推薦
# str.isalnum()            所有字符都是數字或者字母
# str.isalpha()            所有字符都是字母
# str.isdigit()            所有字符都是數字
# str.islower()            所有字符都是小寫
# str.isupper()            所有字符都是大寫
# str.istitle()            所有單詞都是首字母大寫，像標題
# str.isspace()            所有字符都是空白字符、\t、\n、\r


# #### Exercise 1

# In[ ]:


x = 'Hello, World'
print(x[5])  # 請取出字串中的「，」


# #### Exercise 2

# In[ ]:


print('姓名\t座號\t分數\n王小明\t20\t40\n鄭小勳\t21\t100')


# #### Exercise 3

# In[ ]:


a = input('Please Enter a Number: ')
b = input('Please Enter a String: ')
print('You enter: ', a, '&', b)
print('Result is: ', b, '&', a)


# #### Exercise 4

# In[ ]:


(10+15)*7/2


# #### Exercise 5

# In[ ]:


import math
print('when r is 100cm,', '周長為%0.2fcm and' % (100*2*math.pi), '面積為%0.2fcm2' % (100**2*math.pi))


# #### Exercise 6

# In[ ]:


a = int(input('Please enter your score: '))
if a >= 60:
    print('Pass')
else:
    print('Fail')


# #### Exercise 7

# In[ ]:


a = input('Please enter your score: ')
if int(a) >= 95:
    print('You get $2000')
elif 90 <= int(a) <= 94:
    print('You get $1000')
elif 80 <= int(a) <= 89:
    print('You get $500')
else:
    print('You get $0')


# #### Exercise 8

# In[ ]:


y_high = eval(input('What is your height? '))/100
y_weight = eval(input('What is your weight? '))
bmi = y_weight/(y_high**2)

print(bmi)

if bmi < 18.5:
    print('underweight')
elif 18.5 <= bmi < 24:
    print('normal')
elif 24 <= bmi < 27:
    print('overweight')
elif 27 <= bmi < 30:
    print('moderately obese')
elif 30 <= bmi < 35:
    print('severely obese')
else:
    print('very severely obese')


# #### Exercise 9

# In[ ]:


n1 = int(input('Please enter number 1: '))
n2 = int(input('Please enter number 2: '))
n3 = int(input('Please enter number 3: '))
print('最大的數字為:', max(n1, n2, n3))


# #### Exercise 10

# In[ ]:


a = int(input('Please enter a number: '))

fr = 0
for i in range(1, a+1):
    fr += i
else:
    print('1加到%d的總和為%d' % (a, fr))


# #### Exercise 11

# In[ ]:


a = int(input('Please enter a number: '))

fr = 1
for i in range(1, a+1):
    fr *= i
else:
    print('%d的階乘為%d' % (a, fr))


# #### Exercise 12

# In[ ]:


a = int(input('Please enter a number: '))

fr = 0
for i in range(1, a+1):
    fr += i
    if i < a:
        print(i, end = '+')
    else:
        print(i, end = '=')
else:
    print(fr)


# #### Exercise 13

# In[ ]:


import numpy
a1 = int(input('請輸入數字，如不再輸入請打-1: '))
while a1 == -1:
    a1 = int(input('請輸入數字，如不再輸入請打-1: '))
else:
    a2 = []
    while a1 != -1:
        a2.append(a1)
        a1 = int(input('請輸入數字，如不再輸入請打-1: '))
    else:
        print('SUM:\t%d\nMEAN:\t%0.2f\nMAX:\t%d\nN:\t%d' % (sum(a2), numpy.mean(a2), max(a2), len(a2)))


# #### Exercise 14

# In[ ]:


n = int(input('Please enter a number: '))
n = list(range(1, n+1))

print()
print('Questtion A')
for i in n:
    print('*'*i)

print()
print('Questtion B')
for i in n[::-1]:
    print('*'*i)

print()
print('Questtion C')

t = 0
for i in n:
    t = t + i

m = list(range(1, t+1))

t = 0
for i in n:
    for j in range(1, i+1):
        print(m[0+t], end = ' ')
        t = t+1
    print()


# #### Exercise 15

# In[ ]:


for i in range(1, 10):
    for j in range(1, 10):
        print(i, '*', j, '=', i*j, '\t', sep = '', end = ' ')
    print()


# #### Exercise 16

# In[ ]:


import math

n = input('Please enter a number: ')

while n.isdigit() == False:
    n = input('You enter a float, please enter a int: ')
else:
    n = int(n)

if n == 1:
    print('%d is not a prime' % (n))
elif n <= 3:
    print('%d is a prime' % (n))
else:
    for i in range(2, int(math.sqrt(n))+1):
        if n%i == 0:
            print('%d is not a prime' % (n))
            break
    else:
        print('%d is a prime' % (n))


# #### Exercise 17

# In[ ]:


a = input('Please enter a string: ')
while a != 'q':
    print('You enter: %s' % (a))
    a = input('Please enter a string again, or key in q to quit: ')


# #### Exercise 18

# In[ ]:


a = input('Please enter a int: ')
while a.isdigit() == False:
    a = input('You enter a float, please enter a int: ')
else:
    a = int(a)

for i in range(1, a+1):
    if i == 4:
        continue
    print('floor %d' % i)


# #### Exercise 19

# In[ ]:


print('姓名:%s\n年齡:%d\n性別:%s' % ('帳單之門', 99, 'male'))

print()

a = '姓名:{}\n年齡:{}\n性別:{}'
print(a.format('帳單之門', 99, 'male'))


# #### Exercise 20

# In[ ]:


print('%0.2f+%0.2f=%0.2f' % (5.1, 2.3, 5.1+2.3))

print()

for i in range(1, 6):
    for j in range(1, 9):
        print('%d*%d=%2.d' % (i,j,i*j), end = ' ')
    print()

