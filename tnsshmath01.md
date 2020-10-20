# ***歡迎光臨 ~~~*** https://ssur.cc/3D3NC

## https://github.com/
https://github.com/dydytn/20201017

https://github.com/MyFirstSecurity2020




```python
#@title
import time
seconds = time.time()
local_time = time.ctime(seconds+8*3600)
print("現在時間：", local_time)
```

    現在時間： Tue Sep 22 10:52:06 2020


##股票試算


```python
x="動力"
y="6591"
A=55.3 #平均賣價
B=47 #定價
C=2.5 #承銷費
D=0 #溢收
Q=250 # 出資(萬元)
R=1280 #總資金(萬元)
print("------------------------------------")
print(x+"("+y+")")
E=(((1-0.001425-0.003)*A-B)*0.5-C)*0.5 #每股獲利(註1)或虧損(註2)
F=B+C+D #每股成本(即B+C+D)
print("A=平均賣價=",A)
print("B=定價=",B)
print("C=承銷費=",C)
print("D=溢收=",D)
print("------------------------------------")
if ((1-0.001425-0.003)*A-B-C>0):
  E=(((1-0.001425-0.003)*A-B)*0.5-C)*0.5 #每股獲利(註1)或虧損(註2)
  print("E=每股獲利(註)=",E)
  Z="(註)每股獲利=\n{[(1-0.1425%-0.3%)*A-B]*0.5-C}*0.5"
else:
  E=(1-0.001425-0.003)*A-B-C #每股獲利(註1)或虧損(註2)
  print("E=每股虧損(註)=",E)
  Z="(註)每股虧損=\n(1-0.1425%-0.3%)*A-B-C"
print("F=每股成本(即B+C+D)=",F)
print("E/F=報酬率=",int(10000*E/F)/100.0,"%")
print("------------------------------------")
P=100000*E/F
print("Q=出資(萬元)=",Q)
print("R=總資金(萬元)=",R)
print("------------------------------------")
print("P=個資者每十萬元盈虧=",int(P))
print("P*(Q/R)=合資者每十萬元盈虧=",int(P*Q/R))
print("------------------------------------")
print(Z)
print("------------------------------------")

```

    ------------------------------------
    動力(6591)
    A=平均賣價= 55.3
    B=定價= 47
    C=承銷費= 2.5
    D=溢收= 0
    ------------------------------------
    E=每股獲利(註)= 0.7638243749999987
    F=每股成本(即B+C+D)= 49.5
    E/F=報酬率= 1.54 %
    ------------------------------------
    Q=出資(萬元)= 250
    R=總資金(萬元)= 1280
    ------------------------------------
    P=個資者每十萬元盈虧= 1543
    P*(Q/R)=合資者每十萬元盈虧= 301
    ------------------------------------
    (註)每股獲利=
    {[(1-0.1425%-0.3%)*A-B]*0.5-C}*0.5
    ------------------------------------


##[臺灣全民學習平臺](https://taiwanlife.org/?redirect=0)
ckh72@kimo.com/ 54xxxx45


https://fchart.github.io/



###type與identity operators(is is not)與多行字串


```python
a=20
b=20
if (a is b):
  print("Line1:a and b have same identity")
else:
  print("Line1:a and b does not have same identity")

if (id(a)==id(b)):
  print("Line2:a and b have same identity")
else:
  print("Line2:a and b does not have same identity") 
print(id(a)) #id() 函数用于获取对象的内存地址
print(id(b))

a=15
b="Tomson"
print(a,"其type=",type(a),",其id=",id(a))
print(b,"其type=",type(b),",其id=",id(b))

c=float(a)
print(c,"其type=",type(c),",其id=",id(c))

d=2-4j
print(d,"其type=",type(d),",其id=",id(d))

e="""Happy birthday to you.
Happy birthday to you.
Happy birthday, dear Tom.
Happy birthday to you."""
print(e,"其type=",type(e),",其id=",id(e)) 
```

    Line1:a and b have same identity
    Line2:a and b have same identity
    10915104
    10915104
    15 其type= <class 'int'> ,其id= 10914944
    Tomson 其type= <class 'str'> ,其id= 139835192418632
    15.0 其type= <class 'float'> ,其id= 139835201242192
    (2-4j) 其type= <class 'complex'> ,其id= 139835201724144
    Happy birthday to you.
    Happy birthday to you.
    Happy birthday, dear Tom.
    Happy birthday to you. 其type= <class 'str'> ,其id= 139835192321776


##格式化輸出


```python
a=12345.6789
print('%d'%(a))
print('%7d'%(a)) 
print('%7d'%(a))
print('%9.2f'%(a))
print('%10.2e'%(a))
print("%s%s%s%s"%("玩家","戰鬥力","職業","技能"))
print("%3s%6s%4s%4s"%("玩家","戰鬥力","職業","技能"))
print("=========================")
print("%3s%8d%4s%4s"%("王大明",88,"騎士","劈砍"))
print("%3s%8d%4s%4s"%("李小王",10,"新手","無"))
print("%3s%8d%4s%4s"%("林老大",100,"團長","斬殺"))
```

    12345
      12345
      12345
     12345.68
      1.23e+04
    玩家戰鬥力職業技能
     玩家   戰鬥力  職業  技能
    =========================
    王大明      88  騎士  劈砍
    李小王      10  新手   無
    林老大     100  團長  斬殺


###字串


```python
A="welcome to Taipei!"
print(A)
print(A.strip()) #把字符串的第一个字符大写
print(A.lower())

print("編號:{1}(年齡:{2}歲,體重:{0}公斤)".format(65,"101",35))

```

    welcome to Taipei!
    welcome to Taipei!
    welcome to taipei!
    編號:101(年齡:35歲,體重:65公斤)


##序列


```python
A=[87,56,41,99]
print("原始序列=",A)
A.sort()  #呼叫sort
print("遞增序列=",A)
A.reverse() #呼叫reverse
print("遞減序列=",A)
```

    原始序列= [87, 56, 41, 99]
    遞增序列= [41, 56, 87, 99]
    遞減序列= [99, 87, 56, 41]



```python
#https://medium.com/ccclub/ccclub-python-for-beginners-tutorial-bf0648108581
f = open('file_io.txt', 'w')  #寫入檔案
f.write("Try to use file.write()\nHail HYDRA")
f.close()

f = open('file_io.txt')
k = f.readlines()
print(k)
f.close()

!ls  #輸入!ls查看當前路徑下之檔案

```

    ['Try to use file.write()\n', 'Hail HYDRA']
    file_io.txt  out.txt  sample_data


#**判斷閏年與平年**


```python
N=2028
#N=int(input("請輸入西元年度:(輸入後請按enter)"))
if (N%4==0):
  if (N%100==0 and N%400!=0):
     print("西元"+str(N)+"年是平年.")
  else:
     print("西元"+str(N)+"年是閏年.")
else:
  print("西元"+str(N)+"年是平年.") 

```

    西元2028年是閏年.


#**找零程式**


```python
#N=191
N=int(input("請輸入繳費金額(輸入後請按enter):"))
#M=1000
M=int(input("請輸入付款金額(輸入後請按enter):"))
P=M-N
print("收你{}元,需找你{}元,明細如下".format(M,P))
n500=P//500
P=P%500
n100=P//100
P=P%100
n50=P//50
P=P%50
n10=P//10
P=P%10
n5=P//5
P=P%5
n1=P//1
print("找你500元{}張".format(n500))
print("找你100元{}張".format(n100))
print("找你 50元{}個".format(n50))
print("找你 10元{}個".format(n10))
print("找你  5元{}個".format(n5))
print("找你  1元{}個".format(n1))
```

    請輸入繳費金額(輸入後請按enter):191
    請輸入付款金額(輸入後請按enter):2041
    收你2041元,需找你1850元,明細如下
    找你500元3張
    找你100元3張
    找你 50元1個
    找你 10元0個
    找你  5元0個
    找你  1元0個


#***尤拉計畫*** [按此可進入網站](https://projecteuler.net/)

##Problem 1:Multiples of 3 and 5


If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.

Find the sum of all the multiples of 3 or 5 below 1000.

如果我們列出所有低於10的自然數，它們是3或5的倍數，則得到3、5、6和9。這些倍數的總和為23。

找出1000以下3或5的所有倍數的總和。




```python
N=1000
s=0
for i in range(1,N,1):
  if(i%3==0 or i%5==0):
    s=s+i
print(N,"以下3或5的所有倍數的總和=",s)

```

    1000 以下3或5的所有倍數的總和= 233168


##Problem 2:Even Fibonacci numbers

Each new term in the Fibonacci sequence is generated by adding the previous two terms. By starting with 1 and 2, the first 10 terms will be:

1, 2, 3, 5, 8, 13, 21, 34, 55, 89, ...

By considering the terms in the Fibonacci sequence whose values do not exceed four million, find the sum of the even-valued terms.

斐波那契數列中的每個新項都是通過將前兩個項相加而生成的。 從1和2開始，前10個項將是：

1，2，3，5，8，13，21，34，55，89，...

通過考慮斐波那契數列中值不超過400萬的項，找到偶值項的總和。


```python
a=1
b=2
N=4000000
s=0
while a<=N :
  if (a%2==0):
    s=s+a
  #print(a) #檢查用
  c=a+b
  a=b
  b=c
 
print("斐波那契數列中值不超過",N,"的項,為偶值項的總和=",s)
```

    斐波那契數列中值不超過 4000000 的項,為偶值項的總和= 4613732


##Problem 3:Largest prime factor

The prime factors of 13195 are 5, 7, 13 and 29.

What is the largest prime factor of the number 600851475143 ?


13195的主要因子是5、7、13和29。

什麼是600851475143的最大素數？


```python

num=600851475143
i=2
Ans=[]
print(num,"的質因數分解=",end="")
while num > 1:
   if (num % i) == 0:
      Ans.append(i)
      num=num/i
   else :
     i=i+1
print(Ans,",其最大質因數=",max(Ans))
```

    600851475143 的質因數分解=[71, 839, 1471, 6857] ,其最大質因數= 6857


##Problem 4:Largest palindrome product

A palindromic number reads the same both ways. The largest palindrome made from the product of two 2-digit numbers is 9009 = 91 × 99.

Find the largest palindrome made from the product of two 3-digit numbers.

回文數在兩個方向上都相同。 由兩個兩位數的乘積組成的最大回文數為9009 = 91×99。

查找由兩個3位數字的乘積組成的最大回文。


```python
N=3 #兩個N位數乘積(N>=2)
(p,q,r)=(1,1,1)
for a in range(10**N-1,10**(N-1),-1):
  for b in range(a,10**(N-1)-1,-1):
     s1=str(a*b)
     s2=s1[::-1]
     #print(a,"*",b,"=",s1,",其反轉數為",s2,".相等與否:",s1==s2) #check
     if (s1==s2 and a*b>r):
       (p,q,r)=(a,b,a*b)
print(p,"*",q,"=",r)
```

    993 * 913 = 906609


##Problem 5:Smallest multiple

2520 is the smallest number that can be divided by each of the numbers from 1 to 10 without any remainder.

What is the smallest positive number that is evenly divisible by all of the numbers from 1 to 20?

2520是可以除以1到10的每個數字而沒有任何餘數的最小數字。

能被1到20的所有數均分的最小正數是多少？


```python
def lcm(x, y):
   if x > y:
       greater = x
   else:
       greater = y
   while(True):
       if((greater % x == 0) and (greater % y == 0)):
           lcm = greater
           break
       greater += 1
   return lcm
#以下為主程式
N=20
a=1
for i in range(1,N+1,1):
  b=lcm(a,i)
  a=b
print("1,2,3,...",N,"的最小公倍數=",b)
```

    1,2,3,... 20 的最小公倍數= 232792560


##Problem 6:Sum square difference

The sum of the squares of the first ten natural numbers is,$1^2+2^2+3^2+....+10^2=385$

The square of the sum of the first ten natural numbers is,$(1+2+3+....+10)^2=3025$


Hence the difference between the sum of the squares of the first ten natural numbers and the square of the sum is$3025-385=2640$

Find the difference between the sum of the squares of the first one hundred natural numbers and the square of the sum.


```python
N=100
(s1,s2)=(0,0)
for i in range(1,N+1,1):
  s1=s1+i*i
  s2=s2+i
print("Ans=",s2*s2-s1)
```

    Ans= 25164150


##Problem 7:10001st prime
By listing the first six prime numbers: 2, 3, 5, 7, 11, and 13, we can see that the 6th prime is 13.

What is the 10 001st prime number?


```python
N=10001
num=2
n=0
while n<N:
   for i in range(2,int(num**0.5)+1,1):
       if (num % i) == 0:
           break
   else:
       n=n+1
       #print("第",n,"個質數為",num) #check
   num=num+1
print("第",n,"個質數為",num-1)
```

    第 10001 個質數為 104743


##Problem 8 : Largest product in a series

The four adjacent digits in the 1000-digit number that have the greatest product are 9 × 9 × 8 × 9 = 5832.

73167176531330624919225119674426574742355349194934

96983520312774506326239578318016984801869478851843

85861560789112949495459501737958331952853208805511

12540698747158523863050715693290963295227443043557

66896648950445244523161731856403098711121722383113

62229893423380308135336276614282806444486645238749

30358907296290491560440772390713810515859307960866

70172427121883998797908792274921901699720888093776

65727333001053367881220235421809751254540594752243

52584907711670556013604839586446706324415722155397

53697817977846174064955149290862569321978468622482

83972241375657056057490261407972968652414535100474

82166370484403199890008895243450658541227588666881

16427171479924442928230863465674813919123162824586

17866458359124566529476545682848912883142607690042

24219022671055626321111109370544217506941658960408

07198403850962455444362981230987879927244284909188

84580156166097919133875499200524063689912560717606

05886116467109405077541002256983155200055935729725

71636269561882670428252483600823257530420752963450

Find the thirteen adjacent digits in the 1000-digit number that have the greatest product. What is the value of this product?


```python
digits="""
73167176531330624919225119674426574742355349194934
96983520312774506326239578318016984801869478851843
85861560789112949495459501737958331952853208805511
12540698747158523863050715693290963295227443043557
66896648950445244523161731856403098711121722383113
62229893423380308135336276614282806444486645238749
30358907296290491560440772390713810515859307960866
70172427121883998797908792274921901699720888093776
65727333001053367881220235421809751254540594752243
52584907711670556013604839586446706324415722155397
53697817977846174064955149290862569321978468622482
83972241375657056057490261407972968652414535100474
82166370484403199890008895243450658541227588666881
16427171479924442928230863465674813919123162824586
17866458359124566529476545682848912883142607690042
24219022671055626321111109370544217506941658960408
07198403850962455444362981230987879927244284909188
84580156166097919133875499200524063689912560717606
05886116467109405077541002256983155200055935729725
71636269561882670428252483600823257530420752963450"""
digits=digits.replace("\n","")
#print(digits.isdigit()) #檢測字符串是否只由數字組成
#print(len(digits))
N=13
Ans=0
for i in range(0,len(digits)-N+1,1):
  d=1
  for j in range(0,N,1):
    d=d*int(digits[i+j])
  if(d>Ans):
    Ans=d
print("Ans=",Ans)
```

    Ans= 23514624000


##Problem 9: Special Pythagorean triplet

A Pythagorean triplet is a set of three natural numbers, a < b < c, for which,
$a^2+b^2=c^2$
For example, $3^2+4^2=5^2$

There exists exactly one Pythagorean triplet for which a + b + c = 1000.
Find the product abc.


```python
N=1000
for a in range(1,N-1,1):
  for b in range(a,N,1):
    for c in range(b,N+1,1):
      if (a*a+b*b==c*c and a+b+c==1000):
        print("Ans=",a*b*c)
      
```

    Ans= 31875000


##Problem 10 : Summation of primes

The sum of the primes below 10 is 2 + 3 + 5 + 7 = 17.

Find the sum of all the primes below two million.


低於10的質數之和為2 + 3 + 5 + 7 = 17。

找出200萬以下的所有質數之和。


```python
N=2000000
num=3
s=2
while num<N:
   for i in range(2,int(num**0.5)+1,1):
       if (num % i) == 0:
           break
   else:
       s=s+num
   num=num+1
print(N,"以下的質數和為",s)
```

    2000000 以下的質數和為 142913828922


##Problem 11 : Largest product in a grid

In the 20×20 grid below, four numbers along a diagonal line have been marked in red.

08 02 22 97 38 15 00 40 00 75 04 05 07 78 52 12 50 77 91 08

49 49 99 40 17 81 18 57 60 87 17 40 98 43 69 48 04 56 62 00

81 49 31 73 55 79 14 29 93 71 40 67 53 88 30 03 49 13 36 65

52 70 95 23 04 60 11 42 69 24 68 56 01 32 56 71 37 02 36 91

22 31 16 71 51 67 63 89 41 92 36 54 22 40 40 28 66 33 13 80

24 47 32 60 99 03 45 02 44 75 33 53 78 36 84 20 35 17 12 50

32 98 81 28 64 23 67 10 26 38 40 67 59 54 70 66 18 38 64 70

67 26 20 68 02 62 12 20 95 63 94 39 63 08 40 91 66 49 94 21

24 55 58 05 66 73 99 26 97 17 78 78 96 83 14 88 34 89 63 72

21 36 23 09 75 00 76 44 20 45 35 14 00 61 33 97 34 31 33 95

78 17 53 28 22 75 31 67 15 94 03 80 04 62 16 14 09 53 56 92

16 39 05 42 96 35 31 47 55 58 88 24 00 17 54 24 36 29 85 57

86 56 00 48 35 71 89 07 05 44 44 37 44 60 21 58 51 54 17 58

19 80 81 68 05 94 47 69 28 73 92 13 86 52 17 77 04 89 55 40

04 52 08 83 97 35 99 16 07 97 57 32 16 26 26 79 33 27 98 66

88 36 68 87 57 62 20 72 03 46 33 67 46 55 12 32 63 93 53 69

04 42 16 73 38 25 39 11 24 94 72 18 08 46 29 32 40 62 76 36

20 69 36 41 72 30 23 88 34 62 99 69 82 67 59 85 74 04 36 16

20 73 35 29 78 31 90 01 74 31 49 71 48 86 81 16 23 57 05 54

01 70 54 71 83 51 54 69 16 92 33 48 61 43 52 01 89 19 67 48


The product of these numbers is 26 × 63 × 78 × 14 = 1788696.

What is the greatest product of four adjacent numbers in the same direction (up, down, left, right, or diagonally) in the 20×20 grid?


```python
digits="""
08 02 22 97 38 15 00 40 00 75 04 05 07 78 52 12 50 77 91 08
49 49 99 40 17 81 18 57 60 87 17 40 98 43 69 48 04 56 62 00
81 49 31 73 55 79 14 29 93 71 40 67 53 88 30 03 49 13 36 65
52 70 95 23 04 60 11 42 69 24 68 56 01 32 56 71 37 02 36 91
22 31 16 71 51 67 63 89 41 92 36 54 22 40 40 28 66 33 13 80
24 47 32 60 99 03 45 02 44 75 33 53 78 36 84 20 35 17 12 50
32 98 81 28 64 23 67 10 26 38 40 67 59 54 70 66 18 38 64 70
67 26 20 68 02 62 12 20 95 63 94 39 63 08 40 91 66 49 94 21
24 55 58 05 66 73 99 26 97 17 78 78 96 83 14 88 34 89 63 72
21 36 23 09 75 00 76 44 20 45 35 14 00 61 33 97 34 31 33 95
78 17 53 28 22 75 31 67 15 94 03 80 04 62 16 14 09 53 56 92
16 39 05 42 96 35 31 47 55 58 88 24 00 17 54 24 36 29 85 57
86 56 00 48 35 71 89 07 05 44 44 37 44 60 21 58 51 54 17 58
19 80 81 68 05 94 47 69 28 73 92 13 86 52 17 77 04 89 55 40
04 52 08 83 97 35 99 16 07 97 57 32 16 26 26 79 33 27 98 66
88 36 68 87 57 62 20 72 03 46 33 67 46 55 12 32 63 93 53 69
04 42 16 73 38 25 39 11 24 94 72 18 08 46 29 32 40 62 76 36
20 69 36 41 72 30 23 88 34 62 99 69 82 67 59 85 74 04 36 16
20 73 35 29 78 31 90 01 74 31 49 71 48 86 81 16 23 57 05 54
01 70 54 71 83 51 54 69 16 92 33 48 61 43 52 01 89 19 67 48"""
digits=digits.replace("\n","")
digits=digits.replace(" ","")
def a(h,k):
  x=int(digits[(h-1)*n*2+2*k-2])  #十位數字
  y=int(digits[(h-1)*n*2+2*k-1])  #個位數字
  return 10*x+y
n=20
d=4 #d個連乘積
max1=0 #橫向的最大值
max2=0 #直向的最大值
max3=0 #斜率正向的最大值
max4=0 #斜率負向的最大值
"""
for i in range(1,n+1,1):
  for j in range(1,n+1,1):
     print(a(i,j),",",end="")
  print(" ")
"""
for i in range(1,n+1,1):
  for j in range(1,n-d+2,1):
     max1=max([max1,a(i,j)*a(i,j+1)*a(i,j+2)*a(i,j+3)])
print("max1=",max1)

for i in range(1,n-d+2,1):
  for j in range(1,n+1,1):
     max2=max([max2,a(i,j)*a(i+1,j)*a(i+2,j)*a(i+3,j)])
print("max2=",max2)

for i in range(d,n+1,1):
  for j in range(1,n-d+2,1):
     max3=max([max3,a(i,j)*a(i-1,j+1)*a(i-2,j+2)*a(i-3,j+3)])
print("max3=",max3)

for i in range(1,n-d+2,1):
  for j in range(1,n-d+2,1):
     max4=max([max4,a(i,j)*a(i+1,j+1)*a(i+2,j+2)*a(i+3,j+3)])
print("max4=",max4)
print(" Ans=",max([max1,max2,max3,max4]))
```

    max1= 48477312
    max2= 51267216
    max3= 70600674
    max4= 40304286
     Ans= 70600674


##Problem 12:Highly divisible triangular number

The sequence of triangle numbers is generated by adding the natural numbers. So the 7th triangle number would be 1 + 2 + 3 + 4 + 5 + 6 + 7 = 28. The first ten terms would be:

1, 3, 6, 10, 15, 21, 28, 36, 45, 55, ...

Let us list the factors of the first seven triangle numbers:

 1: 1


 3: 1,3


 6: 1,2,3,6


10: 1,2,5,10


15: 1,3,5,15


21: 1,3,7,21


28: 1,2,4,7,14,28


We can see that 28 is the first triangle number to have over five divisors.

What is the value of the first triangle number to have over five hundred divisors?




```python
N=50
n=1
t=1
while n<=N:
  print(t,"th triangle number=",n)
  t=t+1
  n=n+t

```

    1 th triangle number= 1
    2 th triangle number= 3
    3 th triangle number= 6
    4 th triangle number= 10
    5 th triangle number= 15
    6 th triangle number= 21
    7 th triangle number= 28
    8 th triangle number= 36
    9 th triangle number= 45


#**三元一次的聯立方程組(例題)**


```python
#@title
# 三元一次的聯立方程組 (例題1)
from sympy import Symbol, solve
x=Symbol('x')
y=Symbol('y')
z=Symbol('z')

print("例題1")
print("滿足 x+y+z=9 與 2x+3y+4z=29  與 3x+2y-z=8 之解如下:")
print(solve([x+y+z-9,2*x+3*y+4*z-29,3*x+2*y-z-8]))
```

    例題1
    滿足 x+y+z=9 與 2x+3y+4z=29  與 3x+2y-z=8 之解如下:
    {x: 2, y: 3, z: 4}



```python
#@title
# 三元一次的聯立方程組 (例題2)
from sympy import Symbol, solve
x=Symbol('x')
y=Symbol('y')
z=Symbol('z')

print("例題2")
print("滿足 x+y+2z=7 與 2x-y+3z=5  與 4x+y+7z=10 之解如下:")
print(solve([x+y+2*z-7,2*x-y+3*z-5,4*x+y+7*z-10]))
```


```python
#@title
# 三元一次的聯立方程組 (例題3)
from sympy import Symbol, solve
x=Symbol('x')
y=Symbol('y')
z=Symbol('z')

print("例題3")
print("滿足 x-y+z=0 與 x+y+2z=2  與 3x+y+5z=4 之解如下:")
print(solve([x-y+z,x+y+2*z-2,3*x+y+5*z-4]))
```


```python
#@title
# 三元一次的聯立方程組 (演練6)
from sympy import Symbol, solve
x=Symbol('x')
y=Symbol('y')
z=Symbol('z')

print("演練6")
print("滿足 x+3y+2z=2 與 3x-y+2z=1  與 2x+2y-z=-2 之解如下:")
print(solve([x+3*y+2*z-2,3*x-y+2*z-1,2*x+2*y-z+2]))
```

# **座標軸進行設定**

##座標軸1


```python
#@title
import numpy as np
import matplotlib.pyplot as plt
plt.figure(figsize=(16,12),dpi=80)
x=np.linspace(-np.pi,np.pi,100)
y=np.cos(x)
#通过xsticks与yticks函数：指定坐标轴的刻度
plt.xticks(np.linspace(-np.pi,np.pi,20))
plt.yticks(np.linspace(-1,1,20))
 
#绘制颜色为黑色、以点绘制线宽为2.0的线条
plt.plot(x,y,color="blue",linewidth=3.0,linestyle=':')
plt.show()
```

##座標軸2


```python
#@title
import numpy as np
import matplotlib.pyplot as plt

plt.figure(figsize=(4,4),dpi=80)
ax = plt.gca()  
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
plt.xlim(-10, 10)
plt.ylim(-10, 10)

plt.show()
```

# **梅森數 與 梅森質數（Mersenne prime）**
##**梅森數是指形如 $2^n-1$ 的數，記為 $M_n$ ；如果一個梅森數是質數,則稱它為梅森質數截至2018年12月，已知的梅森質數共有51個。已知最大的梅森質數是 $2^{82589933}-1$**

## *前N個梅森數*


```python
#@title
#前N個梅森數
N=100
#N=int(input("Enter a number: "))
print("前",N,"個梅森數:",end="")
for i in range(1,N+1,1):
  print(2**i-1,",",end=" ")
```

    前 100 個梅森數:1 , 3 , 7 , 15 , 31 , 63 , 127 , 255 , 511 , 1023 , 2047 , 4095 , 8191 , 16383 , 32767 , 65535 , 131071 , 262143 , 524287 , 1048575 , 2097151 , 4194303 , 8388607 , 16777215 , 33554431 , 67108863 , 134217727 , 268435455 , 536870911 , 1073741823 , 2147483647 , 4294967295 , 8589934591 , 17179869183 , 34359738367 , 68719476735 , 137438953471 , 274877906943 , 549755813887 , 1099511627775 , 2199023255551 , 4398046511103 , 8796093022207 , 17592186044415 , 35184372088831 , 70368744177663 , 140737488355327 , 281474976710655 , 562949953421311 , 1125899906842623 , 2251799813685247 , 4503599627370495 , 9007199254740991 , 18014398509481983 , 36028797018963967 , 72057594037927935 , 144115188075855871 , 288230376151711743 , 576460752303423487 , 1152921504606846975 , 2305843009213693951 , 4611686018427387903 , 9223372036854775807 , 18446744073709551615 , 36893488147419103231 , 73786976294838206463 , 147573952589676412927 , 295147905179352825855 , 590295810358705651711 , 1180591620717411303423 , 2361183241434822606847 , 4722366482869645213695 , 9444732965739290427391 , 18889465931478580854783 , 37778931862957161709567 , 75557863725914323419135 , 151115727451828646838271 , 302231454903657293676543 , 604462909807314587353087 , 1208925819614629174706175 , 2417851639229258349412351 , 4835703278458516698824703 , 9671406556917033397649407 , 19342813113834066795298815 , 38685626227668133590597631 , 77371252455336267181195263 , 154742504910672534362390527 , 309485009821345068724781055 , 618970019642690137449562111 , 1237940039285380274899124223 , 2475880078570760549798248447 , 4951760157141521099596496895 , 9903520314283042199192993791 , 19807040628566084398385987583 , 39614081257132168796771975167 , 79228162514264337593543950335 , 158456325028528675187087900671 , 316912650057057350374175801343 , 633825300114114700748351602687 , 1267650600228229401496703205375 , 

##*判斷質數與否*


```python
#判斷質數與否
# Program to check if a number is prime or not

num = 407

# To take input from the user
num = int(input("Enter a number: "))

# prime numbers are greater than 1
if num > 1:
   # check for factors
   for i in range(2,int(num**0.5)+1,1):
       if (num % i) == 0:
           print(num,"is not a prime number")
           print(i,"*",num//i,"=",num)
           break
   else:
       print(num,"is a prime number")
       
# if input number is less than
# or equal to 1, it is not prime
else:
   print(num,"is not a prime number")
```

    Enter a number: 5
    5 is a prime number



```python
#從1到N的正整數中為質數者(其中N>=2)
N=50
#N=int(input("Enter a number: "))
print("從1到",N,"的正整數中為質數者:",end="")
for x in range(2,N+1,1):
    # check for factors
     for i in range(2,int(x**0.5)+1,1):
        if (x % i) == 0:
            #print(x,"is not a prime number")
            #print(i,"*",x//i,"=",x)
            break
     else:
        #print(x,"is a prime number")
        print(x,",",end=" ") 
```

    從1到 50 的正整數中為質數者:2 , 3 , 5 , 7 , 11 , 13 , 17 , 19 , 23 , 29 , 31 , 37 , 41 , 43 , 47 , 

##*找前N個梅森數中的質數*


```python
#@title
#找前N個梅森數中的質數
N=50
#N=int(input("Enter a number: "))
print("前",N,"個梅森數:",end="")
for i in range(1,N+1,1):
  print(2**i-1,",",end=" ")
print("")

print("前",N,"個梅森數中是質數者:",end="")
for x in range(2,N+1,1):
     for i in range(2,int((2**x-1)**0.5)+1,1):
        if((2**x-1)%i)==0:
            break
     else:
        print(2**x-1,",",end=" ")
print("")

```

    前 50 個梅森數:1 , 3 , 7 , 15 , 31 , 63 , 127 , 255 , 511 , 1023 , 2047 , 4095 , 8191 , 16383 , 32767 , 65535 , 131071 , 262143 , 524287 , 1048575 , 2097151 , 4194303 , 8388607 , 16777215 , 33554431 , 67108863 , 134217727 , 268435455 , 536870911 , 1073741823 , 2147483647 , 4294967295 , 8589934591 , 17179869183 , 34359738367 , 68719476735 , 137438953471 , 274877906943 , 549755813887 , 1099511627775 , 2199023255551 , 4398046511103 , 8796093022207 , 17592186044415 , 35184372088831 , 70368744177663 , 140737488355327 , 281474976710655 , 562949953421311 , 1125899906842623 , 
    前 50 個梅森數中是質數者:3 , 7 , 31 , 127 , 8191 , 131071 , 524287 , 2147483647 , 


#**生日快樂名單**


```python
#@title
S=["Tom","John","Peter","Alice","Donna"]
for x in S:
   print("Happy birthday to you.")
   print("Happy birthday to you.")
   print("Happy birthday,","dear",x,".")
   print("Happy birthday to you.")
   print(" ")
```


```python
#@title
m=1
m=int(input("請輸入月份數字(1~12):(輸入後請按enter)"))
print(m,"月份壽星名單:",end="")
friend=[[10,"佩屏"],[5,"韻玉"],[4,"曜宇"],[6,"采成"],[2,"秋萍"],[3,"明憲"],\
 [7,"雅君"],[8,"雅雯"],[11,"美菱"],[12,"惠文"],[9,"育亦"],[10,"怡皓"],\
 [1,"靜毓"],[2,"宜欣"],[3,"宗韋"],[12,"雅茹"],[7,"琇娥"],[4,"淑屏"],\
 [8,"政年"],[6,"羿樂"],[11,"亭娥"],[5,"怡君"],[9,"瓊男"],[10,"曜宇"],\
 [3,"雅慈"],[4,"茂元"],[7,"怡英"],[12,"雅婷"],[5,"治威"],[8,"宛真"],\
 [6,"慈成"],[9,"雅真"],[11,"宛真"],[1,"家齊"],[2,"玉華"],[4,"宜屏"],\
 [5,"小原"],[3,"其胤"],[9,"怡恩"],[10,"志名"],[4,"瑋皓"],[7,"俊毓"],\
 [2,"彥瑋"],[12,"韋伶"],[5,"偉哲"],[7,"佳穎"],[6,"皓佐"],[8,"俊偉"],\
 [9,"偉昆"],[11,"俊凡"],[4,"文華"],[3,"建輝"],[1,"琇凱"],[2,"珊英"],\
 [5,"淑娟"],[7,"潔方"]]
for x in friend:
  if x[0]==m:
    print(x[1],",",end="")
print(" ")
print(" ")
```

    請輸入月份數字(1~12):(輸入後請按enter)10
    10 月份壽星名單:佩屏 ,怡皓 ,曜宇 ,志名 , 
     


#**設m,n為小於或等於4的相異正整數且a,b為非零實數﹒**
#**已知函數 $f(x)=ax^m$ 與 $g(x)=bx^n$ 的圖形恰有3個相異交點﹐**
#**請選出可能的選項:**
##**(1)m,n皆為偶數且a,b同號 (2)m,n皆為偶數且a,b異號**
##**(3)m,n皆為奇數且a,b同號 (4)m,n皆為奇數且a,b異號**
##**(5)m,n為一奇一偶﹒** 
###**(106學測)(答:1,3)**


```python
#@markdown 
import numpy as np
import matplotlib.pyplot as plt
plt.figure(figsize=(12,6),dpi=80)
plt.subplot(1,2,1)    #作圖1
plt.title("(a,b)=(1,2);(m,n)=(2,4)") #標題名稱
(a,b)=(1,2);(m,n)=(2,4)
x=np.linspace(-1,1,100)
y1=a*x**m
y2=b*x**n
plt.plot(x,y1,label="$y=ax^m$")
plt.plot(x,y2,label="$y=bx^n$")
plt.legend(loc="upper left")
ax = plt.gca()  
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))

plt.subplot(1,2,2)    #作圖2
plt.title("(a,b)=(1,2);(m,n)=(2,4)") #標題名稱
(a,b)=(1,2);(m,n)=(1,3)
x=np.linspace(-1,1,100)
y1=a*x**m
y2=b*x**n
plt.plot(x,y1,label="$y=ax^m$")
plt.plot(x,y2,label="$y=bx^n$")
plt.legend(loc="upper left")
ax = plt.gca()  
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
plt.show()
```




![png](tnsshmath01_files/tnsshmath01_66_0.png)



#**設x為一正實數且滿足 $x*3^x＝3^{18}$﹔若x落在連續正整數k與k＋1之間﹐則k＝?**
###(94學測)(答:15)


```python
import numpy as np
import matplotlib.pyplot as plt
plt.figure(figsize=(12,6),dpi=80)

x=np.linspace(-5,20,100)
y=x*(3**x)-3**18
plt.plot(x,y)
#plt.plot(x,y,label="$y=x*3^x-3^{18}$")
#plt.legend(loc="upper left")

ax = plt.gca()  
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
plt.xlim(-5,20)
plt.ylim(-1*3**18,3**18)
plt.show()
```




![png](tnsshmath01_files/tnsshmath01_68_0.png)



#**正整數1,2,3,....,N,試求奇數積與偶數積之和?**
##例如N=6,試求1x3x5+2x4x6=?


```python
#@title
N=50 #正偶數
Num=[i for i in range(1,N+1,1)]
a=1;b=1
#print(Num)
for i in range(0,N,1):
  if (i%2==0):
    a=a*Num[i]
  if (i%2==1):
    b=b*Num[i]
print("解法一")
print("N=",N,",其奇數積與偶數積之和=",a+b)

a=1;b=1
for i in range(1,N+1,1):
  if (i%2==1):
    a=a*i
  else:
    b=b*i
print("解法二")
print("N=",N,",其奇數積與偶數積之和=",a+b)
```

    解法一
    N= 50 ,其奇數積與偶數積之和= 578905684082613894746536562390625
    解法二
    N= 50 ,其奇數積與偶數積之和= 578905684082613894746536562390625


#**輸入月份數字(1~12),輸出其月份英文名稱縮寫**


```python
#@title
x=int(input("請輸入月份數字(1~12):(輸入後請按enter)"))
month="JanFebMarAprMayJunJulAugSepOctNovDec"
print(str(x)+"月其英文名稱:",month[3*x-3:3*x])
```

#**攝氏及華氏溫度的轉換**
###華氏=攝氏*(9/5)+32
###攝氏=(華氏-32)*5/9


```python
#@title
x=input("請輸入帶溫度表示符號的溫度值(例如:32C):")
if x[-1] in ["C","c"]:
  y=1.8*float(x[0:-1])+32
  print(x,"=",int(y),"F")
elif x[-1] in ["F","f"]:
  y=(float(x[0:-1])-32)/1.8
  print(x,"=",int(y),"C")
else:
  print("輸入有誤")

```

#**解一元二次方程式 $ax^2+bx+c=0$**


```python
print("解一元二次方程式 a*x*x+b*x+c=0")
a,b,c=eval(input("Please enter the coefficients(a,b,c):"))
print(a,b,c)
D=b*b-4*a*c
if (D>0 and a!=0):
  x1=(-1*b+D**0.5)/(2.0*a)
  x2=(-1*b-D**0.5)/(2.0*a)
  print("有兩相異實數解:",x1,"與",x2)
elif (D==0 and a!=0):
  x1=-1*b/(2.0*a)
  print("有兩相等實數解",x1)
elif D<0:
  print("無實數解")
else:
  print("輸入有誤")

```

    解一元二次方程式 a*x*x+b*x+c=0
    Please enter the coefficients(a,b,c):1,2,0
    1 2 0
    有兩相異實數解: 0.0 與 -2.0


# **尚未分類**


```python
import numpy as np
import matplotlib.pyplot as plt
from ipywidgets import interact,interact_manual
x = np.linspace(0, 2*np.pi, 1000)
def draw(a):
    y = np.sin(x)
    plt.plot(x, y,color="blue")   # y=sin(x)
    y1 = np.sin(a*x)
    plt.plot(x, y1,color="red")   # y=sin(ax)  
    plt.show()

interact(draw,a=(1,5,1))
```




    interactive(children=(IntSlider(value=3, description='a', max=5, min=1), Output()), _dom_classes=('widget-inte…






    <function __main__.draw>



# **Markdown格式**

主標題
====
次標題
----
#字體
##字體
###字體
####字體
#####字體
######字體
#*字體*
#**字體**
#***字體***
* 字體
* 字體
1. 字體







# 第一題 109.09.18 公佈，109.10.02 中午 12 點截止
 有一個大正立方體由 125 個單位立方體所組成，今有一個平面垂直且平分大正立方體內
部之對角線，試問該平面與幾個單位立方體相交？

