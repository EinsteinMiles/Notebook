# 一、基本语法

### python是一种面向对象的解释型语言，是强类型的动态脚本语言

### bug

1. 培养自己识别bug的能力(多看)
2. 培养自己分析bug的能力(多想)
3. 培养自己解决bug的能力(多尝试并记录下来)
4. 有思路写不出代码
   - 先写注释版本
   - 然后尝试翻译成代码
   - 如果卡住了，就写一个更简单的版本

### debug

断点调试

## 1.数据类型

### 01.数字

- 整数 int
- 浮点数 float
- 复数
- 布尔

### 02.字符串  

#### 1‘ 拼接

- 用加号进行拼接

#### 2’字符串格式化

- %s 字符串

  - ```python
    print("%s" % stirng)
    ```

- %d 整型

- %f 浮点型

  ```python
  # 5表示宽度，不常用
  # 2表示精度
  print("%5.2f" % float)
  ```

- 快速格式化

  - f"内容{变量}"
  - 不关心精度控制，也不关心数据类型
  
- 复制：ctrl+d

- 表达式格式化

  - 表达式是一条具有明确执行结果的语句，如1+1

#### 3'字符串操作方法

- 字符串的索引同列表
- 字符串也不可以修改

- replace方法

  ```python
  str.replace(str1,str2)
  # 用str2替换str1
  # 此方法不是修改了字符串本身，而是得到了一个新的字符串
  ```

- split方法

  ```python
  str.split()
  # 将字符串以一定方式切割为 **列表**
  ```

- strip方法

  ```python
  # 去掉首尾指定的字符
  # 只能去掉首尾，不能去掉中间
  ```

### 03.列表

- 如果将函数定义为class的成员，那么函数就称为方法，即在类中定义的函数，不过调用方式不同
- 序列
  - 列表、字符串、元组均可视为序列
  - 序列：内容连续、有序，可使用下标索引的一类数据容器
  - 序列[起始下标：结束下标：步长]
  - 序列的切片不会影响本身，会生成一个新的序列

#### 1‘列表操作方法

- 列表索引

  ```python
  list[num]	# 正向索引从0开始
  list[-num]	# 反向索引从-1开始，最末尾的元素为-1
  list[num1][num2]	# 嵌套列表索引
  ```

- 查询元素下标 

  ```python
  list.index(element)
  ```

- 修改下标索引值

  ```python
  list[subsript] = value
  ```

- 插入元素

  ```python
  list.insert(下标,元素)
  ```

- 在列表末尾追加单个元素

  ```python
  list.append()
  ```

- 在列表末尾追加多个元素

  ```python
  list.extend(数据容器)
  ```

- 删除元素

  ```python
  # del lsit[下标]
  # list.pop(下标)
  # list.remove 删除某元素在列表中的第一个匹配项
  ```

- 统计元素

  ```python
  # list.count 统计元素在列表中的数量
  # len(列表)：统计列表中元素的个数
  ```

### 04.元组

- 不可修改，其余操作和列表一样

- 定义一个元素的元组

  ```python
  tuple1 = (1,)
  ```

### 05.集合

- 不支持重复元素
- 内容无序,不支持下标索引
- 定义:{}，创建空集合：set1 = set()

#### 1‘集合操作方法

- pop()方法

  ```python
  # 随机取出一个元素，取出元素后就不在集合中了
  ```

- 取两个集合的差集

  ```python
  set1.difference(set2)
  ```

- 消除两个集合的差集，set1被修改，set2不变

  ```python
  set1.difference_update(set2)
  ```

- 将两个集合组合成新集合

  ```python
  set1.union(set2)
  ```
  
- 不支持下标索引

### 06.字典

#### 1'定义

- ```python
  {
      key1:value1,
   	key2:value2,
      ...
  }
  dict()
  ```
  
- 不支持重复元素，重复添加就会覆盖原数据

- 字典的key和value可以是任何数据类型，key不能是字典

#### 2'字典操作

- 删除元素

  ```python
  dict.pop(key)
  ```

- 获取全部key和values

  ```python
  dict.keys()
  dict.values()
  ```

- sorted排序

  ```python
  # sorted(数据类型,[reverse=True])，True表示降序
  ```

  - 排序完会变成列表

### 07.数据类型的转换

1. int(x)
2. float(x)
3. str(x)

### 08.序列切片

```python
# 序列[起始下标:结束下标:步长]
# 结束下标不包含在内
```



## 2.注释

### 01.单行注释

- #
- 快捷键 ctrl+/ 

### 02.多行注释

- """   """
- 多行注释一般写在文件开头的位置

## 3.标识符

1. 变量的命名
   - 内容限定：英文、中文、数字、下划线；**不推荐使用中文，数字不可用在开头**
   - 大小写敏感
   - 不可使用关键字
2. 变量命名规范
   - 见名知意：简洁明了
   - 下划线命名法:first_name
   - 英文字母全小写
3. 标识符：变量、类、方法的名字

## 4.运算符

### 01.算数运算符

- / 除
- // 整除
- % 取余
- ** 指数

### 02.赋值运算符

- +=、-=、*=、/=
- %=、**=、//=
- c +=a 等价于 c = c+a，其余同理

## 5.判断语句

### 01.if

- 布尔类型
  - True，除0以外都是真
  - False
  
- 比较运算符
  - ==，!=，>，<，<=，>=
  
- if语句的基本格式

  - ```python
    if condition:
        events
    ```

- if else

  ```python
  if condition:
      events1  
  else:
      events2
  ```

- if elif else

  ```python
  if condition:
      events1
  elif condition:
      events2
  # else也可以省略不写
  else:
      events3
  ```

- 判断语句嵌套

  ```python
  if condition:
      if condition2:
          ...
  ```

## 6.循环语句

### 01.while循环

- ```python
  while loop_condition:
      events1
      events2	
      ...
  ```

- 嵌套

  ```python
  while loop_condition:
      events1
      while loop_condition1:
          events2
  ```

### 02.for循环

- ```python
  for i in D:
      events
  ```

- range

  ```python
  range(num)	#获取一个从0开始，到num结束的数字序列，不含num本身
  range(num1,num2)	#获取一个从num1开始，到num2结束的数字序列，不含num本身
  range(num1,num2,step) #获取一个从num1开始，到num2结束的数字序列，以step为步进，不含num本身
  ```

- 变量作用域

  - 临时变量i，其作用域只限定在循环内部，虽然外部可以访问，但是不建议这么做

- ```python
  for i in D1:
      for i in D2:
  ```

- break and continue

  ```python
  # continue
  # 在循环内遇到continue就结束本次循环，进行下一次循环
  for i in range(num):
      events1
      continue
      events2
  #break
  # 结束循环,嵌套也只结束他所在的那个循环
  for i in range(num):
      events1
      break
  ```

  

## 7.python函数

### 01.函数初步

1. 函数定义

   - 组织好的、可重复利用的、用来实现特定功能的代码块

2. 函数定义

   ```python
   def func_name(param):
       func_body
       return value
   ```

3. 形参和实参

   - 形参：函数在定义时，使用的参数为形参(形式参数)
   - 实参：函数在调用时，使用的参数为实参(实际参数)

4. return

   - 函数中return之后的内容都不执行
   - 无返回值的函数，其实际上是返回了None这个字面量，也可以主动返回None
   - None也可以给暂时不需要值的变量赋值

5. 函数说明

   ```python
   def fun(x,y):
       """
       function instruction
       :param x: instruction of x
       :param y: instruction of y
       :param ...:
       :return: instruction of return
       """
   ```

6. 函数的嵌套

   ```python
   def func1():
       def func2:
           body
           return value2
       body
       return value1
   ```

7. 变量作用域

   - 局部变量只在函数体内部生效
   - 全局变量在整个项目中生效

### 02.global关键字

使用global关键字将函数内的变量声明为全局变量

### 03.函数进阶

#### 1'多返回值

```python
return value1,value2,...
```

#### 2'多种传参方式

- 位置参数

  - 调用函数时根据函数定义式的参数位置来传递参数:fun_c(name,age,gender),调用时依次传参
  - 位置和顺序必须一致

- 关键字参数

  - 调用函数时通过“key = value”形式传递参数
  - 此时无需考虑顺序，但是必须有关键字在值前面

- 缺省参数(默认参数)

  - 用于定义函数，为参数提供默认值，调用函数时可不传入该参数
  - 所有位置参数必须出现在默认参数前
  - 若传入参数，则会修改此默认值

- 不定长参数

  - 可变参数，用于不确定调用的时候会传递多少个参数

    ```python
    """
    所有传入的变量都会被args收集，它会将变量位置字合并成一个元组
    kwargs会将传入的参数组成字典
    """
    
    # 位置不定长
    def func(*args):
        pass
    
    # 关键字不定长,参数必须是键值对
    def func(**kwargs):
        pass
    ```

- 函数作为参数传递

  - 将函数传入的作用在于传入的是计算逻辑，而非数据

- lambda匿名函数

  - 可以定义匿名函数，即无名称的函数

    ```python
    # 无名称的函数只能临时使用一次
    lambda x,y:x+y # 实现x+y的操作
    ```

### 04.文件处理

1. 文件编码

   - 将文本转换成二进制储存起来

2. 文件读取

   ```python
   f = open(name,mode,encoding)
   
   # mode
   #r：只读
   #w：写入，若原文件不存在，创建新文件
   #a:将新内容写入到已有内容之后，若原文件不存在，创建新文件
   
   # 读取文件,若多次调用，则后一次在前一次的基础上进行读取,也可以指定读取的字节数
   f.read()
   f.read(13)
   
   # 读取文件全部行，并封装到列表中
   f.readlines()
   
   # 读取单独一行
   f.readline()
   
   # 关闭文件
   f.close()
   
   # 可以自动关闭文件，防止忘记
   with open(name,mode,encoding) as f:
       f.readlines()
   ```

3. 文件写入

   ```python
   # 调用write，内容并未真正写入文件，而是存在内存缓冲区中
   f.write()
   
   # 内容刷新，将内容真正写入文件，close中内置了flush
   f.flush()
   
   # 文件追加写入
   # 将模式改为a，其余和写入相同
   ```

# 二、面向对象编程

## 1.类

1. 类的属性：定义在类中的变量(成员变量)

2. 类的方法

   - 定义在类中的函数(成员方法) 

     ```python
     class Test:
     	"""
     		__init__()：构造方法
     		1.在创建类的时候，不调用也会自动执行
     		2.在创建对象的时候，会将传入参数自动传递给__init__方法使用
     	""" 
         
         # 声明变量并赋值
         def __init__(self,param1,param2):
             self.param1 = param1
             self.param2 = param2
     ```

   - self表示类自身对象的意思

   - 在方法内部，想要访问类的成员变量，必须使用self,不写的话就会访问到类外面的变量

   - 魔术方法，内置的类方法，拥有各自特殊的功能
   
     ```python
     # 字符串方法 __str__
     # 当类对象需要被转换为字符串时，会输出内存地址；用此方法可以把内存地址还原为字符串
     
     # 小于比较方法__lt__
     # 同时完成大于和小于的比较
     def __lt__(self,other):
         pass
     
     # 小于等于比较方法__le__
     # 用于小于等于或大于等于
     
     # 比较运算符 __eq__
     # ==
     ```

## 2.封装

1. 私有成员和属性：用户无法直接使用

2. 用两个下划线开头来定义私有属性和成员

3. 私有成员无法被类对象使用，但是可以被其他成员使用

   ```python
   def Test:
       def __init__(self,__name):
           self.__name =__name # name为私有属性
   ```
   
## 3.继承

1. 基本语法

   ```python
   # 单继承
   class 类名(父类名):
       pass
   
   #多继承
   class 类名(父类1,父类2,...):
       pass
   # 若多个父类中有同名变量，则继承顺序从左到右，谁在前继承谁
   ```

2. 复写

   ```python
   # 在子类中，重新定义父类的属性或者方法即可
   # 复写后，调用父类成员
   父类名.成员
   super().成员
   ```

3. 类型注解

   ```python
   # 变量的类型注解
   var:type
   可以在注释中实现，在注释中写type:类型
   # 函数和方法的类型注解
   def func(param:type):
       pass
   # 联合注解Union
   from typing import Union
   
   data:Union[type,type,...] = [value1,value2,...]
   ```

## 4.多态

1. 含义

   - 完成某个行为时，使用不同的对象会得到不同的状态

2. 基本语法

   ```python
   # 设计一个抽象类，并不拿来使用，而是定义一个属性和方法
   # 定义子类，在子类中实现具体的属性和方法
   
   # 定义抽象类（接口）
   class AC:
       def cool_wind(self):
           """制冷"""
           pass
   
       def hot_wind(self):
           """制热"""
           pass
   
       def swing_l_r(self):
           """左右摆风"""
           pass
   
   
   # 定义实现具体功能的子类
   class Media_AC(AC):
       def cool_wind(self):
           print("美的空调制冷")
   
       def hot_wind(self):
           print("美的空调制热")
   
       def swing_l_r(self):
           print("美的空调左右摆风")
   
   
   class Gree_AC(AC):
       def cool_wind(self):
           print("格力空调制冷")
   
       def hot_wind(self):
           print("格力空调制热")
   
       def swing_l_r(self):
           print("格力空调左右摆风")
   
   
   def make_cool(ac:AC):
       ac.cool_wind()
   
   
   media_ac = Media_AC()
   gree_ac = Gree_AC()
   
   make_cool(media_ac)
   make_cool(gree_ac)
   ```

# 三、模块

## 1.异常

   ### 01’异常处理

   ```python
try:
    pass	# 可能发生错误的代码
except:
    pass	# 如果出现异常执行的代码

except NameError as e:	# 特定异常
    pass
# 捕获多个异常
try:
    pass
except(e1,e2,e3,...):
    pass

# 捕获全部异常
try:
    pass
except Exception as e:
    pass

# 异常的else和finally
try:
    pass
except:
    pass
else:
    pass	# 如果没有出现异常就执行else后面的代码

finally:
    pass	# 无论是否异常都要执行的代码
   ```

   ### 02'异常的传递性

   - 若func1中没有被捕获，就会传递到func2，直到main函数，如果还没有捕获，程序就会报错

## 2.导入

```python
[from 模块名] import [模块|类|变量|函数|*] [as 别名]
import 模块名
from 模块名 import 类、变量、方法
from 模块名 import *
import 模块名 as 别名
from 模块名 import 功能名 as 别名
```

## 3.自定义模块

### 01.main变量

```python
if __name__ == '__main__':	# 在此下面的代码之只会在直接运行时才会执行，而作为模块导入时就不会执行
    pass
```

### 02.all

```python
__all__ = []	# 如果一个模块文件中有此变量，当使用 from import *导入时，只能导入这个列表中的元素
```

## 4.包

### 01.第三方包

- 一个包就是一个文件夹，该文件夹下包含了一个__init__.py文件，该文件夹可用于包含多个模块文件，同类型功能的集合体
- 主要用来管理模块文件![img](https://api2.mubu.com/v3/document_image/09a45da6-b9af-433f-a752-a7b31e0d613b-19225678.jpg)

### 02.导入

```python
import 包名.模块名
```

### 03.安装

```python
# pip install 包名
# pip install -i 镜像网站 包名
```

# 四、MySql

## 1.数据库结构

库->表->数据

## 2.操作

|         命令         | 代码          |
| :------------------: | ------------- |
|   查看有哪些数据库   | show database |
|      使用数据库      | use 数据库名  |
| 查看数据库内有哪些表 | show tables   |
|         退出         | exit          |

## 3.分类

### 01.数据定义DDL

1. 库的创建删除、表的创建删除等

2. 大小写不敏感

3. 可以单行/多行书写，最后以分号结尾

4. 注释

   ```mysql
   -- 注释内容 --
   
   # 注释内容
   
   /* 
   多行注释 
   */
   
   ```

5. 库管理

   ```mysql
   # 查看数据库
   show databases;
   
   # 使用数据库
   use 数据库名称;
   
   # 创建数据库
   create database 数据库名称 [charset UTF8];
   
   # 删除数据库
   drop database 数据库名称;
   
   # 查看当前使用的数据库
   select database();
   ```

6. 表管理

   ```mysql
   # 查看表
   show tables;
   
   # 删除表
   drop table 表名称;
   drop table if exits 表名称;
   
   # 创建表
   creat table 表名称(列名称 列类型，列名称，列类型);
   
   /*
   列类型
   int float
   varchar(长度) 文本，长度为数字，做长度限制使用
    data(日期) timestamp(时间戳)
    */
   ```

### 02.数据操纵DML

1. 新增数据、删除数据、修改数据

   ```mysql
   # 插入
   insert into 表 [(列1，列2，...)] values(值1，插入值2，....);
   
   # 删除
   delete from 表 [where 条件判断];
   # 条件判断操作符 = < > <= >= !=
   
   # 更新
   update 表名 set 列 = 值 [where 条件判断];
   ```

2. sql中只支持单引号

### 03.数据控制DCL

1. 新增用户、删除用户、密码修改、权限管理

### 04.数据查询DQL

1. 基础查询

   ```mysql
   select 字段列表/* from 表 [where 条件判断];
   ```

2. 分组聚合

   ```mysql
   select 字段|聚合函数 from 表 [where 条件判断] group by 列；
   # 当你的group by写了谁，你才能在select字段中出现谁
   
   /* 聚合函数 
   sum(列)
   avg
   min、max
   count(列|*) 求数量
   */
   ```

3. 排序分页

   ```mysql
   # 使用order by 对指定某个列进行排序
   select 列|聚合函数|* from 表;
   
   /* 聚合函数 
   where
   group by
   order by [asc](升序)[desc](降序)
   limit n[,m] 结果的分页查询
   */
   
   # 关键字要按如上顺序依次书写
   # from->where->group by/聚合函数->select->order by->limit
   ```

# 六、Python高阶技巧

## 1.闭包

1. 在函数嵌套的前提下，内部函数使用了外部函数的变量，并且外部函数返回类内部函数，使用外部函数变量的内部函数称为闭包，闭包是一个函数

2. 使用nonlocal关键字修饰的外部函数的变量才能在内部函数中修改它

3. 使用闭包是为了数据的安全性，变量对于内部函数来说是外部变量，对于外部函数来说是内部变量，除了用内部函数以及重新调用外部函数来修改外，其余方法无法修改

4. 占用内存

## 2.装饰器

1. 装饰器就是一种闭包

2. 在不破坏目标函数原有代码和功能的前提下，为目标函数增加新功能

3. 在原函数上方使用 @ 目标函数来增加装饰器

## 3.设计模式

1. 设计模式是一种编程套路，例如面向对象编程

2. 单例模式

   - 创建类的实例后，就可以得到一个完整的、独立的类对象

   - 保证一个类只有一个实例，并提供一个访问它的全局访问点

3. 工厂模式
   - 大量创建一个类的实例

## 4.多线程

1. 进程

   - 就是一个程序，运行在系统之上
   - 多任务运行
   - 不同的进程拥有不同的内存空间

2. 线程

   - 归属于进程，一个进程可以有多个线程，例如下载程序，是进程的实际工作最小单位
   - 多线程运行
   - 线程之间是内存共享的

3. 并行执行

   - 多进程并行执行、多线程并行执行

4. 多线程编程

   ```python
   import threading
   
   thread_obj = threading.Thread([group] [,target [,name[,args[,kwargs]]]])
   """
   group:暂时无用，未来功能的预留参数
   target:执行的目标任务名
   args:以元组方式传参
   kwargs:以字典方式传参
   name:线程名，一般不设置
   """
   
   thread_obj.start()
   ```

# 七、数据结构

## 一、数组

### 1.一维数组

1. 数组定义
   - 一组相关变量能一个接一个存储在内存的一块连续区域内
   - 单元：数组中的每个位置，编号从0开始
   - python中，每个Unicode字符占用两个字节
   - 1个字节(byte) = 8个位(bit)⇒1B = 8b

2. 数组的引用

   - 数组中的每个单元必须占据相同数量的字节，以便时间复杂度为$O(1)$

   - 对象引用：通过引用储存的地址来索引相关的数据，因为地址的位是固定长度的

3. 线性结构
   - 有序数据项的集合，每个数据项都有唯一的前驱和后继
   - 新的数据加入到原有的某个数据项之前或之后
   - 线性结构的区别在于数据项的增减方式

4. 拷贝

   - 浅拷贝：拷贝后，修改数据，原数据也会被改变，因为两者地址是相同的
   - 深拷贝：拷贝后数据和原数据地址不同

5. 紧凑数组

   - 使用的内存少

     - 原始数据在内存中连续存放，而不是存储地址

   - ```python
     # 定义紧凑数组
     import array
     # data type查表可得
     sample = array("data type",[data])
     ```

6. 动态数组和摊销

   - 动态数组
     - 例如列表这种可以改变长度的数组，其占用的内存大小也是不定的
     
     - 数组的长度比对应的列表长度大，用来预留列表可能加入的数据，当预留内存用完时，会重新请求一个更大的内存并释放原来的内存
     
     - 实现动态数组基本上靠list
     
     - ```python
       """
       1.分配一个更大的数组B(一般是旧数组大小的2倍)
       2.设B[i] = A[i]
       3.设A=B
       4.在新的数组里添加元素
       """
       
       class DynamicArray:
           def __init__(self):
               self._n = 0
               self._capacity = 1
               self._A = self._make_array(self._capacity)
       
           def __len__(self):
               return self._n
       
           def __getitem__(self, k):
               if not 0 <= k < self._n:
                   raise IndexError("invalid index")
       
               raise self._A[k]
       
           def append(self, obj):
               if self._n == self._capacity:
                   self._resize(2 * self._capacity)
       
               self._A[self._n] = obj
               self._n += 1
       
           def _resize(self, c):
               B = self._make_array(c)
               for k in range(self._n):
                   B[k] = self._A[k]
       
               self._A = B
               self._capacity = c
       
           # 创建一个底层数组
           def _make_array(self, c):
               return (c * ctypes.py_object)()
       ```
     
   - 摊销

     - 在动态数组中进行增添操作，效率很高
     - 将计算机视为一个投币装置，对每个固定的运行时间支付一枚网络硬币，每进行一次操作，都要有足够的网络硬币来支付。则：网络硬币总数和计算的运行时间成正比

7. 插入排序算法

   - 从数组的第一个元素开始(单个元素无需排序)，将第[n+1]个与前[n]个比较，直至完全排序完毕

   - 时间复杂度为$O(n^2)$

   - ```python
     def insertion_sort(A):
         for k i rang(1,len(a)):
             j = k
             cur = A[k]
             while j > 0 and A[j-1] > cur:
                 A[j] = A[j-1]
                 j -= 1
        		A[j] = cur

### 2.多维数组

1. 二维数组亦称矩阵，第一个索引表示行号，第二个表示列号，且都从0开始

2. 创建二维列表

   ```python
   # 创建一个c行r列，元素为None的二维列表
   data = [[None] * c for j in rang(r)]
   ```

## 二、链表

### 1.单链表

1. 第一个和最后一个数据项需要显式的标记出来，为中间位置的数据提供相对位置

2. 节点(Node)：链表的最基本元素

   - 数据项本身

   - 指向下一个节点的引用数据

   - 节点实现

     ```python
     class Node:
         def __init__(self,init_data):
             self.data = init_data
             self.next = None
     
         def get_data(self):
             return self.data
     
         def get_next(self):
             return self.next
     
         def set_data(self,new_data):
             self.data = new_data
     
         def set_next(self,new_next):
             self.next = new_next
     
     ```

   - 无序表的实现

     ```python
     class UnorderedList:
     
         def __init__(self):
     
             # 设置表头
             self.head = None
     
     
         def add(self,item):
             temp = Node(item)
             temp.set_next(self.head)
             self.head = temp
     
         def size(self):
             current = self.head
             count = 0
     
             while current is not None:
                 count += 1
                 current= current.get_next()
     
             return count
     
         def search(self,item):
             current = self.head
             found = False
     
             while current is not None and not found:
     
                 if current.get_data() == item:
                     found = True
                 else:
                     current = current.get_next()
     
             return found
     
         def remove(self,item):
             current = self.head
             previous = None
             found = False
     
             while not found:
                 if current.get_data() == item:
                     found = True
     
                 else:
                     previous = current
                     current = current.get_next()
     
             if previous is None:
                 self.head = current.get_next()
     
             else:
                 previous.set_next(current.get_next())
     ```
     
   - 有序表的实现
   
     ```python
     class OrderedList:
         def __init__(self):
             self.head = None
     
         def size(self):
             current = self.head
             count = 0
     
             while current is not None:
                 count += 1
                 current = current.get_next()
     
             return count
     
         def remove(self, item):
             current = self.head
             previous = None
             found = False
     
             while not found:
                 if current.get_data() == item:
                     found = True
     
                 else:
                     previous = current
                     current = current.get_next()
     
             if previous is None:
                 self.head = current.get_next()
     
             else:
                 previous.set_next(current.get_next())
     
         def search(self, item):
             current = self.head
             found = False
             stop = False
     
             while current is not None and not found and not stop:
     
                 if current.get_data() == item:
                     found = True
                 else:
                     if current.get_data() > item:
                         stop = True
                     else:
                         current = current.get_next()
     
             return found
     
         def add(self, item):
             current = self.head
             previous = None
             stop = False
     
             # 发现插入位置
             while current is not None and not stop:
                 if current.get_data() > item:
                     stop = True
                 else:
                     previous = current
                     current = current.get_next()
     
             temp = Node(item)
             # 插在表头
             if previous is None:
                 temp.set_next(self.head)
                 self.head = temp
             # 插在表中
             else:
                 temp.set_next(current)
                 previous.set_next(temp)
     ```
   
     

### 2.双链表

## 三、栈和队列

### 1.栈

1. 数据项的加入和移除只能发生在一端，顶端叫【顶top】，底端叫【底base】

2. 后进先出LIFO

3. 反转次序：出栈和入栈的顺序相反

4. 栈的操作

   ```python
   class Stack:
       def __init__(self):
           self.items = []  # 空栈
       
       def push(self, item):
           """入栈"""
           self.items.append(item)
       
       def pop(self):
           """出栈"""
           if not self.is_empty():
               return self.items.pop()
           else:
               raise IndexError("栈为空")
       
       def peek(self):
           """查看栈顶元素"""
           if not self.is_empty():
               return self.items[-1]
           else:
               return None
       
       def is_empty(self):
           """判断栈是否为空"""
           return len(self.items) == 0
       
       def size(self):
           """返回栈的大小"""
           return len(self.items)
   
   # 定义空栈
   my_stack = Stack()
   
   # 最简单的定义空栈
   stack = []
   ```

5. 波兰表达式和逆波兰表达式

   - 波兰表达式：操作符在前，操作数在后
   - 逆波兰表达式：操作符在后，操作数在前

### 2.队列

1. 新数据想的添加发生在尾端(rear)，而现存数据项的移除发生在首端(front)

2. 先进先出(FIFO)

3. 队列仅有一个入口和一个出口，即数据项不能从中间插入

4. 队列操作

   ```python
   # 创建一个空队列
   Queue()
   
   # 将数据项item添加到队尾，无返回值
   enqueue(item)
   
   # 从队首移除数据项，返回值为队首数据项，队列被修改
   dequeue()
   
   # 测试是否为空队列
   is_empty()
   
   # 返回队列中数据项个数
   size()
   
   # 用列表实现queue
   class Queue:
       def __init__(self):
           self.items =[]
   
       def is_empty(self):
           return  self.items == []
   
       def enqueue(self,item):
           self.items.insert(0,item)
   
       def dequeue(self):
           self.items.pop()
   
       def size(self):
           return len(self.items)
   ```

### 3.双端队列

1. 和队列相似，但是数据可以从首或尾进出

2. 并不具有先进先出和后进先出的特性

3. 双端队列操作

   ```python
   class Deque:
   
       def __init__(self):
           """创建一个双端队列"""
           self._items: list = []
   
       def is_empty(self):
           """判断双端队列是否为空"""
           return not bool(self._items)
   
       def add_front(self, item):
           """从队首添加item"""
           self._items.append(item)
   
       def add_rear(self, item):
           """从队尾添加item"""
           self._items.insert(0, item)
   
       def remove_front(self):
           """从队首移除item"""
           return self._items.pop()
   
       def remove_rear(self):
           """从队尾移除item"""
           return self._items.pop(0)
   
       def size(self):
           """返回双端队列中数据项的个数"""
           return len(self._items)
   ```

## 四、哈希表

## 五、树

## 六、图

# 八、算法

## 一、算法分析

### 1.算法分析原理

1. 分析算法效率
   - 算法的效率不依赖于软硬件
   - 通过不需要实现的高层次算法描述来执行算法
   - 考虑可能的所有输入
2. 原子操作
   - 给对象指定一个标识符
   - 确定与这个标识符相关联的对象
   - 执行算术运算
   - 比较两个数的大小
   - 通过索引访问python列表的一个元素
   - 调用函数
   - 从函数返回
3. 通过计算原子操作的执行次数，用t作为算法执行时间的度量
4. 将算法和函数联系在一起，用输入大小n代表原子操作的数量

### 2.算法分析使用的函数

1. 常数函数

   - f(n) = c

2. 对数函数

   - $x = log_bn$
     
   - 在计算机中，底数为2，可表示为$logn$
   - 对于正整数n，用n除以b，只有当结果小于等于1时才停止除法操作，函数值为n除以b的次数
   
3. 线性函数

   - f(n) = n 

4. $nlogn$函数

   - f(n) = $nlogn$

5. 二次函数

   - $f(n) = n^2$
   
6. 指数函数

   - $f(n) = b^n$
   
7. 三次函数和其他多项式

   - $f(n) = \sum_{i=0}^{d}a_in_i$
   
8. 基本函数增长率

   - ![](https://img-blog.csdnimg.cn/20200304092256939.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1RoZV9Pbmx5X0dvZA==,size_16,color_FFFFFF,t_70)

### 3.渐进分析

1. 大O符号
   - 令f(n) $\leq$cg(n)，当n$\geq {n_0} $，称f(n)是O(g(n))
   - 上式中，f(n)、g(n)为正实数映射正整数的函数且c>0，$n_0 \geq 1$
   - 其含义是：当给定一个常数因子且在渐进意义上n趋近于无穷时，f(n)$\leq$g(n),f(n)是g(n)的量级
   - 忽略函数的常量因子和低阶项
2. 比较分析
   - 在使用大O符号时，应注意被“隐藏”的常数因子和低阶项
   - 区分运行时间$O(n^c)$是否为快速算法，只需看是否满足$c>1$，区分$O(b^n)$是否为快速算法，只需看是否满足$b>1$
3. 大$\Omega$符号
   - 令f(n) $\geq$cg(n)，当n$\geq {n_0} $，称f(n)是$\Omega(g(n))$,g(n)是O(f(n))

## 二、递归

### 1.递归

1. 定义

   - 一个函数在执行过程中一次或多次调用其本身，或者通过一种数据结构在其表示中依赖于相同类型的结构更小的实例

2. 二分查找

   - 在一个含有n个元素的有序序列中查找目标值

   - 实现

     ```python
     # 如果目标值等于[mid]的数据，查找成功
     # 如果目标值<[mid]的数据，对前半部分序列重复这一过程，反之亦然
     ```

   - 二分查找算法的复杂度为$O(logn)$

3. 递归思维

   - 从"怎么做" → 到"如何分解"
   - 信任递归：相信递归调用能解决子问题
   - 关注关系：大问题与小问题之间的关系

### 2.递归的类型

1. 线性递归
   - 一个函数执行一个递归调用
2. 二路递归
   - 一个函数执行两个递归调用
3. 多重递归
   - 一个函数执行两次以上的递归调用

### 3.设计递归算法

1. 明确函数功能，写递归之前要先找规律，这样可以明确原子问题

2. 测试一组基本情况，这些基本情况应该被定义，以便后面的递归可以使用，基本情况中不能使用递归

3. 进行递归
   - 递归函数中不能单独定义变量，否则调用的时候会重置变量的值

   ```python
   #找规律：分析问题结构，发现自相似性
   #定关系：建立大问题与小问题的递推关系
   #找基础：确定最简单的基本情况
   #写代码：根据规律实现递归函数
   #验证：用测试用例验证正确性
   ```

4. 递归经典模式

   ```python
   # 模式1：递减模式
   def f(n):
       if n == 0: return base_case
       return n + f(n-1)
   
   # 模式2：分治模式  
   def f(data):
       if len(data) == 1: return base_case
       left = f(data[:mid])
       right = f(data[mid:])
       return combine(left, right)
   
   # 模式3：选择模式
   def f(choices, path):
       if satisfied: return result
       for choice in choices:
           path.append(choice)
           f(choices, path)
           path.pop()
   ```

5. 回溯算法

   ```python
   def backtrack(path, choices):
       if 满足条件:
           结果.append(path)
           return
       for 选择 in 选择列表:
           if 选择合法:
               做选择(path, 选择)
               backtrack(path, 新选择列表)
               撤销选择(path, 选择)
   ```

### 4.消除尾递归

1. 递归的某些形式可以在不使用任何辅助存储空间的情况下被消除，尾递归就是这种形式之一
2. 尾递归必须是线性递归。递归调用后没有任何其他操作
3. python不支持尾递归优化

## 三、排序

## 四、图算法

