自己参考网络资料编写的python教程，侵删

> 参考：
>
> - https://github.com/walter201230/Python
> - https://www.runoob.com/python3/python3-tutorial.html
> - 看漫画学python

**主要目录如下：**

[toc]

# 1. Python简介

Python 是著名的“龟叔” Guido van Rossum 在 1989 年圣诞节期间，为了打发无聊的圣诞节而编写的一个编程语言。国内社区通常将Guido van Rossum简称为“龟叔”，“龟”的发音取自Guido中的“Gui”。

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106222457511.png" alt="image-20221106222457511" style="zoom: 25%;" />

Python的历史大致如下。目前通用的是python3版本。

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106222741751.png" alt="image-20221106222741751" style="zoom:33%;" />

Python 是高级编程语言，它有一个特点就是能快速的开发。Python 为我们提供了非常完善的基础代码库，覆盖了网络、文件、GUI、数据库、文本等大量内容，被形象地称作“内置电池（batteries included）”。用 Python 开发，许多功能不必从零编写，直接使用现成的即可。而且 Python 还能开发网站，多大型网站就是用 Python 开发的，例如 YouTube、Instagram，还有国内的豆瓣。很多大公司，包括 Google、Yahoo 等，甚至 NASA（美国航空航天局）都大量地使用 Python。

当然，任何编程语言有有点，也有缺点，Python 也不例外。那么 Python 有哪些缺点呢？

- 第一个缺点就是运行速度慢，和C程序相比非常慢，因为Python是解释型语言，你的代码在执行时会一行一行地翻译成CPU能理解的机器码，这个翻译过程非常耗时，所以很慢。而C程序是运行前直接编译成CPU能执行的机器码，所以非常快。
- 第二个缺点就是代码不能加密。如果要发布你的 Python 程序，实际上就是发布源代码。像 JAVA , C 这些编译型的语言，都没有这个问题，而解释型的语言，则必须把源码发布出去。

# 2. Python的安装



## Windows下的安装

todo

## Linux下的安装

todo

# 3.第一个Python程序

```python
print('Hello Python')
```

在终端上运行下面的命令：

```shell
python hello.py
```

# 4.Python的注意事项

- 采用UTF-8 编码

  ```python
  #-*-coding:utf-8-*-
  ```

- 具有严格的缩进，Tab

- 大小写敏感

- 与C、C++不同，每一行代码的结尾不用分号；

- 注释：通过用自己熟悉的语言，在程序中对某些代码进行标注说明，这就是注释的作用，能够大大增强程序的可读性

  单行注释：

  以#单独一行开头，或者在一行代码后面注释

- 多行注释：

  ‘’‘ ---

  xxx

  -- ’‘’

# 5. Python 中的变量 #

## 1. 变量的创建和赋值 ##

在Python中为一个变量赋值的同时就声明了该变量，该变量的数据类型就是赋值数据所属的类型，该变量还可以接收其他类型的数据。

在 Python 程序中，变量是用一个变量名表示，可以是任意数据类型，变量名必须是大小写英文、数字和下划线（_）的组合，且不能用数字开头，比如：

```python
a = 88
b = 3.141
c = 'string'
d = ['a',123,12.13,[123,111]] # list
e = ('a',123,12.13,[123,111]) # tuple
```

- 这里的 `a` 就是一个变量，代表一个整数。

- 在 Python 中 `=` 是赋值语句，跟其他的编程语言也是一样的。

- 注意一点是 Python 是不用声明数据类型的，因此可以把任意的数据类型赋值给变量，且同一个变量可以反复赋值，而且可以是不同的数据类型。

- 可以使用type(变量的名字)，来查看变量的类型



## 2. 多个变量赋值 ##

Python 允许同时为多个变量赋值。例如：

```python
a = b = c = 1
```

以上实例，创建一个整型对象，值为 1，**三个变量被分配到相同的内存空间上**。

当然也可以为多个对象指定多个变量。例如：

```python
a, b, c = 1, 2, "liangdianshui"
```

以上实例，两个整型对象 1 和 2 的分配给变量 a 和 b，字符串对象 "liangdianshui" 分配给变量 c。

## 3. 命名规则

**驼峰命名**

- 小驼峰式命名法（lower camel case）： 第一个单词以小写字母开始；第二个单词的首字母大写，例如：myName、aDog

- 大驼峰式命名法（upper camel case）： 每一个单字的首字母都采用大写字母，例如：FirstName、LastName

- 不过在程序员中还有一种命名法比较流行，就是用下划线“_”来连接所有的单词，比如send_buf



## 4. 关键字

关键字，是python已经使用的了，所以不允许开发者自己定义和关键字相同的名字的标示符。

```python
 and     as      assert     break     class      continue    def     del
      elif    else    except     exec      finally    for         from    global
      if      in      import     is        lambda     not         or      pass
      print   raise   return     try       while      with        yield
```

可以通过以下命令进行查看当前系统中python的关键字:

```python
import keyword
keyworld.kwlist
```

# 6. 输入和输出

## 1. 输入

```python
# input()接受表达式输入，并把表达式的结果赋值给等号左边的变量
a = input('提示信息：')
```

- **返回字符串**
- 与int函数结合使用，为变量赋整数值。

- 与float函数结合使用，为变量赋浮点数值。

## 2. 格式化输出

```python
age = 18
name = "xiaohua"
print("我的姓名是%s,年龄是%d"%(name,age))
```

| 格式符号 |             转换             |
| :------: | :--------------------------: |
|    %c    |             字符             |
|    %s    | 通过str() 字符串转换来格式化 |
|    %i    |       有符号十进制整数       |
|    %d    |       有符号十进制整数       |
|    %u    |       无符号十进制整数       |
|    %o    |          八进制整数          |
|    %x    |   十六进制整数（小写字母）   |
|    %X    |   十六进制整数（大写字母）   |
|    %e    |     索引符号（小写'e'）      |
|    %E    |     索引符号（大写“E”）      |
|    %f    |           浮点实数           |
|    %g    |       ％f和％e 的简写        |
|    %G    |        ％f和％E的简写        |





# 7. 基本数据类型

整型（int）、浮点数（float）、字符串（string）、布尔值（boll）、空值(None)



## 整型

```python
a = 100
```



## 浮点数

```python
a = 100.1
```



## 复数类型

整数和浮点数（小数）在数学中被统称为实数。与实数对应的是复数，复数在数学中被表示为：a+bi，其中a被称为实部，b被称为虚部，i被称为虚数单位。复数在数学、理论物理学和电气工程等方面应用广泛，例如向量就可以使用复数表示。

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106224424410.png" alt="image-20221106224424410" style="zoom: 50%;" />



## 字符串

string 使用‘ ’ 或者“ ”括起来的元素

### 字符串创建

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106232845582.png" alt="image-20221106232845582" style="zoom: 33%;" />

字符串：双引号或者单引号中的数据

```python
str1 = "100"
str2 = "abc"
str3 = "a'b'c"
print(str1)
print(str2)
print(str3)

>100
>abc
>a'b'c
```

### 字符串输出

```python
print("姓名：%s"%name)
```

### 字符串输入

```python
userName = input('请输入用户名:')
```

### 字符串索引

```python
name = 'abcdef'
print(name[0])
```



### 字符串切片

`切片`是指对操作的对象截取其中一部分的操作。**字符串、列表、元组**都支持切片操作。

**切片的语法**：[起始:结束:步长]

**注意：选取的区间属于左闭右开型，即从"起始"位开始，到"结束"位的前一位结束（不包含结束位本身)。**

我们以字符串为例讲解。

如果取出一部分字符串，则可以在中括号[]中使用:

```python
name = 'abcdef'
print(name[0:3]) # 取 下标0~2 的字符
```



### 字符串的常见操作

| 函数                                          | 说明                                                         |
| --------------------------------------------- | ------------------------------------------------------------ |
| mystr.find(str, start=0, end=len(mystr))      | 检测 str 是否包含在 mystr中，如果是返回开始的索引值，否则返回-1 |
| mystr.rfind(str, start=0,end=len(mystr) )     | 类似于 find()函数，不过是从右边开始查找.                     |
| mystr.index(str, start=0, end=len(mystr))     | str是否在mystr中                                             |
| mystr.rindex( str, start=0,end=len(mystr))    | 类似于 index()，不过是从右边开始.                            |
| mystr.count(str, start=0, end=len(mystr))     | 返回 str在start和end之间 在 mystr里面出现的次数              |
| mystr.replace(str1, str2,  mystr.count(str1)) | 把 mystr 中的 str1 替换成 str2,如果 count 指定，则替换不超过 count 次 |
| mystr.split(str=" ", 2)                       | 以 str 为分隔符切片 mystr，如果 maxsplit有指定值，则仅分隔 maxsplit 个子字符串 |
| mystr.capitalize()                            | 把字符串的第一个字符大写                                     |
| mystr.title()                                 | 把字符串的每个单词首字母大写                                 |
| mystr.startswith(obj)                         | 检查字符串是否是以 obj 开头, 是则返回 True，否则返回 False   |
| mystr.endswith(obj)                           | 检查字符串是否以obj结束，如果是返回True,否则返回 False.      |
| mystr.lower()                                 | 转换 mystr 中所有大写字符为小写                              |
| mystr.upper()                                 | 转换 mystr 中的小写字母为大写                                |
| mystr.ljust(width)                            | 返回一个原字符串左对齐,并使用空格填充至长度 width 的新字符串 |
| mystr.rjust(width)                            | 返回一个原字符串右对齐,并使用空格填充至长度 width 的新字符串 |
| mystr.center(width)                           | 返回一个原字符串居中,并使用空格填充至长度 width 的新字符串   |
| mystr.lstrip()                                | 删除 mystr 左边的空白字符                                    |
| mystr.rstrip()                                | 删除 mystr 字符串末尾的空白字符                              |
| mystr.strip()                                 | 删除mystr字符串两端的空白字符                                |
| mystr.partition(str)                          | 把mystr以str分割成三部分,str前，str和str后                   |
| mystr.rpartition(str)                         | 类似于 partition()函数,不过是从右边开始.                     |
| mystr.splitlines()                            | 按照行分隔，返回一个包含各行作为元素的列表                   |
| mystr.isalpha()                               | 如果 mystr 所有字符都是字母 则返回 True,否则返回 False       |
| mystr.isdigit()                               | 如果 mystr 只包含数字则返回 True 否则返回 False              |
| mystr.isalnum()                               | 如果 mystr 所有字符都是字母或数字则返回 True,否则返回 False  |
| mystr.isspace()                               | 如果 mystr 中只包含空格，则返回 True，否则返回 False.        |
| mystr.join(str)                               | mystr 中每个字符后面插入str,构造出一个新的字符串             |
| max(str)                                      | 返回字符串 *str* 中最大的字母。                              |
| min(str)                                      | 返回字符串 *str* 中最小的字母。                              |
| 加（+）                                       | 加（+）运算符可以将两个序列连接起来，                        |
| 乘（*）                                       | 乘（*）运算符可以将两个序列重复多次。                        |
| in                                            | 元素在str中返回True                                          |
| not in                                        | 元素不在str中返回True                                        |



## bool

Python 中，可以直接用 True、False 表示布尔值（请注意大小写）

False : 0,' ',[],{},

布尔值可以用 `and`、`or` 和 `not` 运算。



## 空值

在 Python 中，用 `None `来表示



## 转义字符

| 转义字符    | 描述                                                     |
| :---------- | :------------------------------------------------------- |
| \(在行尾时) | 续行符                                                   |
| \\          | 反斜杠符号                                               |
| \'          | 单引号                                                   |
| \"          | 双引号                                                   |
| \a          | 响铃                                                     |
| \b          | 退格(Backspace)                                          |
| \e          | 转义                                                     |
| \000        | 空                                                       |
| \n          | 换行                                                     |
| \v          | 纵向制表符                                               |
| \t          | 横向制表符                                               |
| \r          | 回车                                                     |
| \f          | 换页                                                     |
| \oyy        | 八进制数，y 代表 0~7 的字符，例如：\012 代表换行。       |
| \xyy        | 十六进制数，以 \x 开头，yy代表的字符，例如：\x0a代表换行 |
| \other      | 其它的字符以普通格式输出                                 |

## 数据类型转换 ##

Python 中基本数据类型转换的方法有下面几个。

| 方法                   | 说明                                                  |
| ---------------------- | ----------------------------------------------------- |
| int(x [,base ])        | 将x转换为一个整数                                     |
| float(x )              | 将x转换到一个浮点数                                   |
| complex(real [,imag ]) | 创建一个复数                                          |
| str(x )                | 将对象 x 转换为字符串                                 |
| repr(x )               | 将对象 x 转换为表达式字符串                           |
| eval(str )             | 用来计算在字符串中的有效 Python 表达式,并返回一个对象 |
| tuple(s )              | 将序列 s 转换为一个元组                               |
| list(s )               | 将序列 s 转换为一个列表                               |
| chr(x )                | 将一个整数转换为一个字符                              |
| unichr(x )             | 将一个整数转换为 Unicode 字符                         |
| ord(x )                | 将一个字符转换为它的整数值                            |
| hex(x )                | 将一个整数转换为一个十六进制字符串                    |
| oct(x )                | 将一个整数转换为一个八进制字符串                      |

比如 `int()` 函数，将符合规则的字符串类型转化为整数 。

```python
str1 = "100"
str2 = "200"
print(str1 + str2)
print(int(str1) + int(str2))

>100200
>300
```

type(<object>)用于判断对象的类型，返回结果可为str、int、float、list等。



## 算术运算符

下面以a=10 ,b=20为例进行计算

| 运算符 |  描述  | 实例                                                         |
| :----- | :----: | ------------------------------------------------------------ |
| +      |   加   | 两个对象相加 a + b 输出结果 30                               |
| -      |   减   | 得到负数或是一个数减去另一个数 a - b 输出结果 -10            |
| *      |   乘   | 两个数相乘或是返回一个被重复若干次的字符串 a * b 输出结果 200 |
| /      |   除   | x除以y b / a 输出结果 2                                      |
| %      |  取余  | 返回除法的余数 b % a 输出结果 0                              |
| **     |   幂   | 返回x的y次幂 a**b 为10的20次方， 输出结果 100000000000000000000 |
| //     | 取整除 | 返回商的整数部分 9//2 输出结果 4 , 9.0//2.0 输出结果 4.0     |

## 赋值运算符

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106225325442.png" alt="image-20221106225325442" style="zoom:50%;" />

## 关系运算符

python中的比较运算符如下表

| 运算符 | 描述                                                         | 示例                                              |
| :----- | :----------------------------------------------------------- | :------------------------------------------------ |
| ==     | 检查两个操作数的值是否相等，如果是则条件变为真。             | 如a=3,b=3则（a == b) 为 true.                     |
| !=     | 检查两个操作数的值是否相等，如果值不相等，则条件变为真。     | 如a=1,b=3则(a != b) 为 true.                      |
| <>     | 检查两个操作数的值是否相等，如果值不相等，则条件变为真。     | 如a=1,b=3则(a <> b) 为 true。这个类似于 != 运算符 |
| >      | 检查左操作数的值是否大于右操作数的值，如果是，则条件成立。   | 如a=7,b=3则(a > b) 为 true.                       |
| <      | 检查左操作数的值是否小于右操作数的值，如果是，则条件成立。   | 如a=7,b=3则(a < b) 为 false.                      |
| >=     | 检查左操作数的值是否大于或等于右操作数的值，如果是，则条件成立。 | 如a=3,b=3则(a >= b) 为 true.                      |
| <=     | 检查左操作数的值是否小于或等于右操作数的值，如果是，则条件成立。 | 如a=3,b=3则(a <= b) 为 true.                      |



## 逻辑运算符

`and` 运算是与运算，只有所有都为 True，and 运算结果才是 True。

`or` 运算是或运算，只要其中有一个为 True，or 运算结果就是 True。

`not` 运算是非运算，它是一个单目运算符，把 True 变成 False，False 变成 True。



## 位运算符

位运算是以二进位（bit）为单位进行运算的，操作数和结果都是整数类型的数据。

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106225032012.png" alt="image-20221106225032012" style="zoom: 25%;" />



## 运算符的优先级

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106225716413.png" alt="image-20221106225716413" style="zoom: 33%;" />



# 判断语句和循环语句



## If语句

`注意`：第一行后面的冒号“:”

### if

```python
if 条件1:
	语句1
```

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106231139901.png" alt="image-20221106231139901" style="zoom: 25%;" />



###  if-else

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106231424779.png" alt="image-20221106231424779" style="zoom: 50%;" />

```python
if 条件1:
	语句1
else:
	语句2
```

### if--elif-else

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106231514175.png" alt="image-20221106231514175" style="zoom: 50%;" />

```python
if 条件1:
   语句1
elif 条件2:
   语句2
else:
   语句3
```

### if嵌套

```python
if 条件1:
	语句1
    if 条件2:
		语句2 
```



## while循环

```python
while 条件1:
        条件满足时，做的事情1
```



## for循环

for循环可以遍历任何序列的项目，如一个string，list ，tuple，set或者dict等。

```python
for 变量 in 可迭代对象:
    语句
```



## break和continue

- break的作用：用来结束整个循环
- continue的作用：用来结束本次循环，紧接着执行下一次的循环
- break/continue只能用在循环中，除此以外不能单独使用
- break/continue在嵌套循环中，只对最近的一层循环起作用



# List #



## 1. 什么是 List 

List （列表）是 Python 内置的一种数据类型，类似于C/C++的数组。 它是一种有序的集合，可以随时添加和删除其中的元素。



## 2. 创建 List ##

从上面的例子可以分析出，列表的格式是这样的。

其实列表就是用**中括号 `[]`** 括起来的数据，里面的每一个数据就叫做元素。每个元素之间使用逗号分隔。

**列表的数据元素可以是不同的数据类型**。

比如：

```python
list = []
list1 = ['两点水','twowter','liangdianshui',123]
list('hello')
list(tuple1)
```

**列表的嵌套**

一个列表中的元素又是一个列表，那么这就是列表的嵌套

```python
    schoolNames = [['北京大学','清华大学'],
                    ['南开大学','天津大学','天津师范大学'],
                    ['山东大学','中国海洋大学']]
```

## 3. 访问list

```python
a = list[index]  #访问列表的某个元素

b= list[start:end]  #访问列表的[start，end）元素
```



## 4. 修改list

```python
list[index] = obj       # 重新赋值
list.append(obj)        #在列表末尾添加新的对象                                      
list.extend(seq)        #在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表） 
list.insert(index, obj) #将对象插入列表                                            


```



## 5. 删除list

```python
list.pop(obj=list[-1])  #移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
del list[index]  		#删除列表的某个元素                 
list.remove(obj)  		#根据元素的值进行删除,并且不返回任何值 
```



## 6. List运算符 ##

列表对 `+`  和 `*`  的操作符与字符串相似。`+` 号用于组合列表，`*`  号用于重复列表。

| Python 表达式                  | 结果                         | 描述                 |
| ------------------------------ | ---------------------------- | -------------------- |
| [1, 2, 3] + [4, 5, 6]          | [1, 2, 3, 4, 5, 6]           | 组合                 |
| ['Hi!'] * 4                    | ['Hi!', 'Hi!', 'Hi!', 'Hi!'] | 复制                 |
| 3 **in** [1, 2, 3]、**not in** | True                         | 元素是否存在于列表中 |
| for x in [1, 2, 3]: print x,   | 1 2 3                        | 迭代循环遍历         |



## 7. List 常用的函数 ##

| 函数&方法         | 描述                                                         |
| ----------------- | ------------------------------------------------------------ |
| len(list)         | 列表元素个数                                                 |
| max(list)         | 返回列表元素最大值                                           |
| min(list)         | 返回列表元素最小值                                           |
| list(seq)         | 将元组转换为列表                                             |
| list.count(obj)   | 统计某个元素在列表中出现的次数                               |
| list.index(obj)   | 从列表中找出某个值第一个匹配项的索引位置                     |
| list.reverse()    | 反向列表中元素                                               |
| list.sort([func]) | 按特定顺序重新排列，默认为由小到大，参数reverse=True可改为倒序，由大到小。 |



# tuple #



## 1、什么是tuple ##

上一节刚说了一个有序列表 List ，现在说另一种有序列表叫**元组**：tuple 。

tuple 和 List 非常类似，但是 **tuple 一旦初始化就不能修改**。

元组（tuple） 不可变是指当你创建了 tuple 时候，它就不能改变了，也就是说它也没有 append()，insert() 这样的方法，但它也有获取某个索引值的方法，但是不能赋值。

那么为什么要有 tuple 呢？

那是因为 tuple 是不可变的，所以代码更安全。

所以建议能用 tuple 代替 list 就尽量用 tuple 。



## 2、创建tuple ##

元组创建很简单，只需要在括号**`()`**中添加元素，并使用逗号隔开即可。

```python
tuple1=('两点水','twowter','liangdianshui',123,456)
tuple(list1)
tuple('hello')
```

创建空元组

```python
tuple3=()
```

**元组中只包含一个元素时，需要在元素后面添加逗号**

```python
tuple4=(123,)
```

如果不加逗号，创建出来的就不是 元组（tuple），而是指 ```123``` 这个数了。


这是因为括号 () 既可以表示元组（tuple），又可以表示数学公式中的小括号，这就产生了歧义。



## 3、访问tuple ##

元组下标索引也是从 0 开始，元组（tuple）可以使用下标索引来访问元组中的值。

```python
#-*-coding:utf-8-*-
tuple1=('两点水','twowter','liangdianshui',123,456)
tuple2='两点水','twowter','liangdianshui',123,456

print(tuple1[1])
print(tuple2[0])
```



## 4、修改tuple ##

可能看到这个小标题有人会疑问，上面不是花了一大段来说 tuple 是不可变的吗？

这里怎么又来修改 tuple （元组） 了。

那是因为元组中的元素值是不允许修改的，但我们可以对元组进行连接组合，还有通过**修改其他列表的值从而影响 tuple 的值。**

具体看下面的这个例子：

```python
#-*-coding:utf-8-*-
list1=[123,456]
tuple1=('两点水','twowater','liangdianshui',list1)
print(tuple1)
list1[0]=789
list1[1]=100
print(tuple1)
```

输出的结果：

```
('两点水', 'twowater', 'liangdianshui', [123, 456])
('两点水', 'twowater', 'liangdianshui', [789, 100])
```


可以看到，两次输出的 tuple 值是变了的。我们看看 tuple1 的存储是怎样的。


![](http://twowaterimage.oss-cn-beijing.aliyuncs.com/2019-08-31-%E4%BF%AE%E6%94%B9tuple%E6%B5%81%E7%A8%8B%E5%9B%BE.png)


可以看到，tuple1 有四个元素，最后一个元素是一个 List ，List 列表里有两个元素。

当我们把 List 列表中的两个元素 `124` 和 `456` 修改为 `789` 和 `100` 的时候，从输出来的 tuple1 的值来看，好像确实是改变了。

但其实变的不是 tuple 的元素，而是 list 的元素。

tuple 一开始指向的 list 并没有改成别的 list，所以，tuple 所谓的“不变”是说，tuple 的每个元素，指向永远不变。注意是 tupe1 中的第四个元素还是指向原来的 list ，是没有变的，我们修改的只是列表 List 里面的元素。



## 5、删除 tuple ##

tuple 元组中的元素值是不允许删除的，但我们可以使用 del 语句来删除整个元组

```python
#-*-coding:utf-8-*-

tuple1=('两点水','twowter','liangdianshui',[123,456])
print(tuple1)
del tuple1
```



## 6、tuple运算符 ##

与字符串一样，元组之间可以使用 `+` 号和 `*` 号进行运算。这就意味着他们可以组合和复制，运算后会生成一个新的元组。

| Python 表达式                 | 结果                         | 描述         |
| ----------------------------- | ---------------------------- | ------------ |
| (1, 2, 3) + (4, 5, 6)         | (1, 2, 3, 4, 5, 6)           | 连接         |
| ('Hi!',) * 4                  | ('Hi!', 'Hi!', 'Hi!', 'Hi!') | 复制         |
| 3 in (1, 2, 3)                | True                         | 元素是否存在 |
| for x in (1, 2, 3):  print(x) | 1 2 3                        | 迭代         |



## 7、元组内置函数 ##

| 方法                        | 描述                    |
| --------------------------- | ----------------------- |
| len(tuple1)                 | 计算元组元素个数        |
| max(tuple1)                 | 返回元组中元素最大值    |
| min(tuple1)                 | 返回元组中元素最小值    |
| tuple(seq)                  | 将列表转换为元组        |
| tuple1.index(obj,strat,end) | obj在tuple1中的索引     |
| tuple1.count(obj)           | tuple1中obj的元素的个数 |



# dict

## 1. 什么是dict 字典

字典是另一种可变容器模型，且可存储任意类型对象。

字典的每个键值 **key:value** 对用冒号 **:** 分割，每个键值对之间用逗号 **,** 分割，整个字典包括在花括号 **{}** 中 ,格式如下所示：

```python
d = {key1 : value1, key2 : value2 }
```



- 字典中找某个元素时，是根据`key`来进行查找的
- 字典里的元素没有顺序
- 字典里的`key`不能重复，`value`可以重复，如果重复最后的一个键值对会替换前面的，值不需要唯一。
- `value`可以取任何数据类型，但`key`必须是不可变的，如string，数字或tuple（list不可以）。



## 2. 创建dict

```python
tinydict1 = { 'abc': 456 }
tinydict2 = { 'abc': 123, 98.6: 37 }
```



## 3. 访问dict

把相应的键放入熟悉的方括弧，如下:

```python
tinydict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}  
tinydict['Name'] 
tinydict['Age']
```

- 如果用dict里没有的`key`访问数据，会输出错误
- dict1.get(key1) # 获取不存在的key1，获取到空的内容，不会出现异常



## 4. 修改dict

向字典添加新内容的方法是增加新的键/值对

```python
tinydict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
tinydict['Age'] = 8 # 更新
tinydict['School'] = "RUNOOB" # 添加
```



## 5. 删除dict

```python
tinydict = {'Name': 'Zara', 'Age': 7, 'Class': 'First'}
 
del tinydict['Name']  # 删除键是'Name'的条目
tinydict.clear()      # 清空字典所有条目
del tinydict          # 删除字典
```



## 6. 字典内置函数&方法

Python字典包含了以下内置函数：

| 序号 | 函数                | 描述                                             |
| :--- | :------------------ | ------------------------------------------------ |
| 1    | cmp(dict1, dict2）  | 比较两个字典元素                                 |
| 2    | len(dict1)          | 计算字典元素个数，即键的总数                     |
| 3    | str(dict1)          | 输出字典可打印的字符串表示                       |
| 4    | type(variable)      | 返回输入的变量类型，如果变量是字典就返回字典类型 |
| 5    | dict1.keys()        | 返回一个包含字典所有key的列                      |
| 6    | dict1.values()      | 返回一个包含字典所有value的列表                  |
| 7    | dict1.items()       | 返回一个包含所有（键，值）元祖的列表             |
| 8    | dict1.has_key(key1) | 如果key在字典中，返回True，否则返回False         |

Python字典包含了以下内置方法：

| 序号 | 函数及描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | dict.clear()删除字典内所有元素                               |
| 2    | dict.copy()返回一个字典的浅复制                              |
| 3    | [dict.fromkeys(seq[, val])创建一个新字典，以序列 seq 中元素做字典的键，val 为字典所有键对应的初始值 |
| 4    | [dict.get(key, default=None)](https://www.runoob.com/python/att-dictionary-get.html) 返回指定键的值，如果值不在字典中返回default值 |
| 5    | [dict.has_key(key)](https://www.runoob.com/python/att-dictionary-has_key.html) 如果键在字典dict里返回true，否则返回false |
| 6    | [dict.items()](https://www.runoob.com/python/att-dictionary-items.html) 以列表返回可遍历的(键, 值) 元组数组 |
| 7    | [dict.keys()](https://www.runoob.com/python/att-dictionary-keys.html) 以列表返回一个字典所有的键 |
| 8    | [dict.setdefault(key, default=None)](https://www.runoob.com/python/att-dictionary-setdefault.html) 和get()类似, 但如果键不存在于字典中，将会添加键并将值设为default |
| 9    | [dict.update(dict2)](https://www.runoob.com/python/att-dictionary-update.html) 把字典dict2的键/值对更新到dict里 |
| 10   | [dict.values()](https://www.runoob.com/python/att-dictionary-values.html) 以列表返回字典中的所有值 |
| 11   | [pop(key[,default\])](https://www.runoob.com/python/python-att-dictionary-pop.html) 删除字典给定键 key 所对应的值，返回值为被删除的值。key值必须给出。 否则，返回default值。 |
| 12   | [popitem()](https://www.runoob.com/python/python-att-dictionary-popitem.html) 返回并删除字典中的最后一对键和值。 |



# set

## 1. 什么是set

集合（set）是一种可迭代的、无序的、不能包含重复元素的容器类型的数据。

## 2. 创建set

我们可以通过以下两种方式创建集合。
1 set（iterable）函数：参数iterable是可迭代对象（字符串、列表、元组、集合和字典等）。
2 {元素1，元素2，元素3，⋯}：指定具体的集合元素，元素之间以逗号分隔。对于集合元素，需要使用大括号括起来。

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106234054308.png" alt="image-20221106234054308" style="zoom:33%;" />

## 3. 修改集合

修改集合类似于修改列表，可以向其中插入和删除元素。修改可变集合有如右所示的常用方法。
set1.add(elem)：添加元素，如果元素已经存在，则不能添加，不会
抛出错误。
set1.remove(elem)：删除元素，如果元素不存在，则抛出错误。
set1.clear()：清除集合。

# imort

在Python中一个模块就是一个文件，模块是保存代码的最小单位，在模块中可以声明变量、函数、属性和类等Python代码元素。

- import＜模块名＞：通过这种方式会导入<模块名>的所有代码元素，在访问时需要加前缀“模块名.”

  <img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106223752073.png" alt="image-20221106223752073" style="zoom:33%;" />

- from＜模块名＞import＜代码元素＞：通过这种方式会导入m2中的x变量，在访问时不需要加前缀“m2.”

  <img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106223811710.png" alt="image-20221106223811710" style="zoom:33%;" />

- from＜模块名＞import＜代码元素＞as＜代码元素别名＞：与②类似，在当前m1模块的代码元素（x变量）与要导入的m2模块的代码元素（x变量）名称有冲突时，可以给要导入的代码元素（m2中的x）一个别名x2

<img src="C:\Users\李雅\AppData\Roaming\Typora\typora-user-images\image-20221106223825550.png" alt="image-20221106223825550" style="zoom:33%;" />



