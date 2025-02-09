# python_syntax
### 資料型別
- **整數(Inetger),浮點數(Floating-Point Number),布林(Boolean),字串(String)**
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
- **型別轉換**
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
- **不一樣的資料型別無法做運算**
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
- 宣告變數
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
- **查看變數的記憶體位址**
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
- **變數命名規則:要避開python的函式名稱,否則無法使用該函式**
  ```
  print = 3
  print(1+2)
  ```
  - 輸出
  ```
  TypeError: 'int' object is not callable
  ```
- **變數的加減乘除**
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
- **沒有定義就做運算**
  ```
  f=f+2
  ```
  - 輸出
  ```
  NameError: name 'f' is not defined
  ```
- **除法除數不可為0**
  ```
  print(2%0,2//0)
  ```
  - 輸出
  ```
  integer division or modulo by zero
  ```
- **比較運算符**
  - `or` 返回第一個為 `True` 的值，或者都是`false`則回傳最後一個操作數。
  - `and` 返回第一個為 `False` 的值，或者都是`True`則回傳最後一個操作數。
  ```
  print("abc"=="abc")
  print("abc">"abc")
  print("abc"<"b")
  print("abc"<"abcd")
  print("Eng"<"中文")
  print(not 5>4)
  print(5>4 and 4<3)
  print(5>4 or 4<3)
  print(3 or 2)
  print(1 and 2)
  print(0 and 2)
  print(0 or 2)
  print(0 or 0)
  a=4
  print(3<a<6)
  print(3<a and a<6)
  print(3<a<6>(a+1))
  print(3<a and a<6 and 6>(a+1))
  ```
  - 輸出
  ```
  True
  False
  True
  True
  True
  False
  False
  True
  3
  2
  0
  2
  0
  True
  True
  True
  True
  ```
- **複合指定運算**
  ```
  a=6
  a-=1
  print(a)
  a%=3
  print(a)
  b=10
  b+=a
  print(b)
  c=100
  c/=b
  print(c)
  c%=a
  print(c)
  ```
  - Tips:通常來說運算規則為先乘除後加減,括號最優先,同層級則由左至右
  - python內建函式
  - 
  ```
  #取絕對值
  print(abs(-2.5))
  #取最小值
  print(min(1,2))
  #取最大值
  print(max(1,2,3))
  #pow(a,b,c),a的b次方並除以取餘數
  print(pow(2,3))
  print(pow(2,3,5))
  #round(a,b),a取到小數點後第b位,沒有填b則取到整數位
  print(round(1.3578,2))
  print(round(1.3578))
  ```
  - 輸出
  ```
  2.5
  1
  3
  8
  3
  1.36
  1
  ```
### 容器(list,tuple,set,dict)
- **list**
  ```
  a = [0,1,2]
  print(a)
  print(a[0])
  a[1]='abc'
  print(a)
  print(a[1])
  #a[-n],倒數第n個
  a[-1]='def'
  print(a[-1])
  print(a)
  #多層list
  fruit = [['apple',80],['banana',67],['orange',89]]
  print(fruit[0])
  print(fruit[0][0])
  print(fruit[0][1])
  human = [['abner',['abc135','167','55']],['shawn',['feg835','177','65']]]
  print(human[0][0],human[0][1][1],human[0][1][2])
  ```
  - 輸出
  ```
  [0, 1, 2]
  0
  [0, 'abc', 2]
  abc
  def
  [0, 'abc', 'def']
  ['apple', 80]
  apple
  80
  abner 167 55
  ```
  - **Slicing切片**
  ```
  #slicing切片
  a=b=[0,1,2,3,4,5,6,'name']
  #讀取1到3位置的資料
  print(a[1:3])
  #讀取第4個到第4個的資料,不會有資料
  print(a[4:4])
  #讀取倒數第5個到第3個的資料
  print(a[-5:4])
  #讀取倒數第5個到倒數第3個的資料
  print(a[-5:-3])
  #讀取到倒數第3個到最後一個的資料
  print(a[-3: ])
  #把第1個到第(3-1)個取代為5,'ab'
  b[1:3]=[5,'ab']
  print(b)
  #把第2個到最後一個取代為空的資料
  b[2:]=[ ]
  print(b)
  #在位置為1的地方插入新串列,會取代位置1的資料
  b[1:1]=[8,9]
  print(b)
  #在位置為1的地方插入9
  b[1]=[9]
  print(b)
  #逆著讀取資料
  print(a[-3: :-1])
  s=[0,1,2,3,4,5,6]
  #順著讀取從第1個到第6個的資料,間隔為2(0,2,4,6)
  print(s[0:7:2])
  #逆著讀取從第4個到第1個的資料
  print(s[4:1:-1])
  #倒著印出串列
  print(s[ : :-1])
  c=[0,1,2,3,4,5,6]
  #先將"abc"轉為list,所以會變成['a','b','c']再先將"abc"轉為list再從第1個到最後一個,都替換為該串列
  c[1:]="abc"
  print(c)
  #先將"ab"轉為list,所以會變成['a','b','c']再從第1個到第(4-1)個,每兩個一數替換為['a','b']
  c[1:4:2]="ab"
  print(c)
  #使用slicing刪除資料
  d=[0,1,2,3,4,5]
  del d[1]
  print(d)
  del d[2:5]
  print(d)
  del d[1:6:2]
  print(d)
  del a
  print(d)
  print([1,2]<[1,2,3])
  #英文字母會比較unicode的大小
  print(['x','y']<['z'])
  ```
  - 輸出
  ```
  [1, 2]
  []
  [3]
  [3, 4]
  [5, 6, 'name']
  [0, 5, 'ab', 3, 4, 5, 6, 'name']
  [0, 5]
  [0, 8, 9, 5]
  [0, [9], 9, 5]
  [[9], 0]
  [0, 2, 4, 6]
  [4, 3, 2]
  [6, 5, 4, 3, 2, 1, 0]
  [0, 'a', 'b', 'c']
  [0, 'a', 'b', 'b']
  [0, 2, 3, 4, 5]
  [0, 2]
  [0]
  [0]
  True
  True
  ```
- **tuple**
- **set**
- **dict**
### 流程控制
- 
### 實戰
- 
