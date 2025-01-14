# python_syntax
### 資料型別
- 整數(Inetger),浮點數(Floating-Point Number),布林(Boolean),字串(String)
```
#1.23乘以10的n次方
print(1.23e10)
#1.23乘以10的-n次方
print(1.23e-4)
#布林值,若為真則輸出True,反之為False
print(1>2)
print(1<2)
print((1+1)==2)
#string可使用'或",使用"""允許輸出混和'及"的字串
print("a hole new world")
print('a hole new world')
print("""hello'a'hole"new"world""")
```
- 輸出
```
12300000000.0
0.000123
False
True
True
a hole new world
a hole new world
hello'a'hole"new"world
```
- 型別轉換
```
#布林可轉為整數型態True==1,False==0
print(int(True)+1)
print(int(False)+1)
#整數可轉為浮點數,一樣的資料型態才開始做運算
print(1+2.1)
print(10-5.8)
print(5.8+10)
print(1+int('2'))
print(1+float('3'))
print(str(10.0)+'2')
print(2+int('123'))
```
- 輸出
```
2
1
3.1
4.2
15.8
3
4.0
10.02
125
```
- 不一樣的資料型別無法做運算
- 字串加整數
```
print('1'+int(True))
```
- 輸出
```
TypeError: can only concatenate str (not "int") to str
```
- 布林加字串
```
print(True+str(1))
```
- 輸出
```
print(True+str(1))
```
- 變數
```
#宣告整數變數,檢查資料型別
age=18
print(age)
print(age+1)
type(age)
old = age
print(old)
#宣告浮點數變數,檢查資料型別
pi=3.14159
r=1.23456
print(2*r*pi)
print(pi*r*r)
print(type(pi),type(r),type(pi*r*r),type(2*r*pi))
#宣告字串變數,檢查資料型別
st='child'
print(type(st))
mi = None
print(mi)
print(type(mi))
```
- 輸出
```
18
19
18
7.7569627008
4.788217935949825
<class 'float'> <class 'float'> <class 'float'> <class 'float'>
<class 'str'>
None
<class 'NoneType'>
```
- 刪除變數
```
mi = None
print(mi)
print(type(mi))
del mi
print(mi)
```
- 輸出
```
None
<class 'NoneType'>
NameError: name 'mi' is not defined
```
- 查看變數的記憶體位址
```
#id(a)是用來查看a變數的記憶體位址,每次執行可能會不一樣
a=b=5
print(id(a),id(b),id(5))
c=5;d=6
print(id(c),id(d))
c='abcd'
print(type(c))
```
- 輸出
```
133002860839280 133002860839280 133002860839280
133002860839280 133002860839312
<class 'str'>
```
- 變數命名規則:要避開python的函式名稱,否則無法使用該函式
```
print = 3
print(1+2)
```
- 輸出
```
TypeError: 'int' object is not callable
```
- 變數的加減乘除
```
#變數的加減乘除
a=b=10
a=a+4
a=a-1
b=b+a
b=b-a
print(a,b)
c,d,e=11,12,13
print(c,d,e)
print(2*3.0)
print(4/2,5/2,10//2,50%10,4.4//2,3.4%2)
print(False+1,True/2)
#開平方根或立方根
print(100**0.5,8**(1/3))
```
- 輸出
```
13 10
11 12 13
6.0
2.0 2.5 5 0 2.0 1.4
1 0.5
10.0 2.0
```
- 沒有定義就做運算
```
f=f+2
```
- 輸出
```
NameError: name 'f' is not defined
```
- 除法除數不可為0
```
print(2%0,2//0)
```
- 輸出
```
integer division or modulo by zero
```
- 比較運算符
```
```
### 資料結構(容器)
### 流程控制
### 函式
