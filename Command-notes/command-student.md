# 编程学习笔记

## 一、基础知识——概念
### 1. 操作符
* **逻辑操作符(Logical Operators):**

  等于:`==`

  不等于:`!=`

  大于:`>`

  大于等于:`>=`

  小于:`<`

  小于等于:`<=`

  属于:`in`

* **数值操作符有：**

  `+、-、*、/、//、%、**` —— 它们分别代表加、减、乘、除、商、余、幂

  **完整的操作符优先级列表，参见 [官方文档](https://docs.python.org/3/reference/expressions.html#operator-precedence)。**

* **布尔值操作符：**  
  `与、或、非：and、or、not`它们之中，优先级最低的是或 or，然后是与 and, 优先级最高的是非 not。

  **操作符优先级：** 数值计算的操作符优先级最高，其次是逻辑操作符，布尔值的操作符优先级最低。

* **值的类型及转换：**  
1. 将字符串转换为数字用: `int()、float()`
2. 将数字转换成字符串用: `str()`
3. 将整数转换成浮点数字用: `float()`
4. 将浮点数字转换成整数用: `int()`
5. 查看某个值属于什么类型:`type()`


* **字符串的三种操作：**

1. 拼接：`+` 和 `' '`（后者是空格）
2. 拷贝：`*`
3. 逻辑运算：`in、not in`；以及，`<、<=、>、>=、!=、==`

    > *[这一章主要介绍了基础数据类型的运算细节。而除了基础数据类型，我们需要由它们组合起来的更多复杂数据类型。但无论数据的类型是什么，被操作符操作的总是该数据的值。所以，虽然绝大多数编程书籍按照惯例会讲解 “数据类型”，但为了究其本质，我们在这里关注的是 “值的类型”。虽然只是关注焦点上的一点点转换，但实践证明，这一点点的不同，对初学者更清楚地把握知识点有巨大的帮助。](https://github.com/selfteaching/the-craft-of-selfteaching/blob/b20e3b092696cc0e098377345ffc56063768d7eb/Part.1.E.2.values-and-their-operators.ipynb)*

* **[python说明书](https://docs.python.org/zh-cn/3.7/)**
---

### 2. 命令符
* **Bash常用命令说明：**  

  Name | Method
  ----- | -----
  `cd` | Change Directory 的缩写，转到指定目录；
  `ls` | List 的缩写，列出当前目录中的内容；
  `mkdir` | Make Directory 的缩写，在当前目录中创建一个新的目录；
  `pwd` | Present Working Directory 的缩写，显示当前工作目录；
  `touch` | 创建一个指定名称的空文件；
  `rm` | Remove 的缩写，删除指定文件；
  `rmdir` | Remove Directory 的缩写，删除指定目录；
  `cp` | Copy 的缩写，拷贝指定文件；
  `mv` | Move 的缩写，移动指定文件；
  `cat` | Concatenate 的缩写，在屏幕中显示内容；
  `chmod` | Change Mode 的缩写，改变文件的权限；
  `man` | Manual 的缩写，显示指定命令的使用说明；
  `ren` | 文件重命名；


---
### 3. 常用函数  
>**[python常需查看的标准库](https://docs.python.org/zh-cn/3/library/index.html)**  
**[python内置函数说明书](https://docs.python.org/zh-cn/3/library/functions.html)**  
**[python内置类型说明书](https://docs.python.org/zh-cn/3/library/stdtypes.html)**  

* **常用内建函数：**

>`divmod(n, m)`: 用来计算`n`除以`m`，返回两个整数，一个是商，另外一个是余。  
`pow(n, m)`: 用来做乘方运算，返回`n`的`m`次方。  
`round(n)`: 返回离浮点数字`n`最近的那个整数。

* **print:**


>`print(*object, sep=' ', end='\n', file=sys.stdout, flush=False)`  
`sep=' '`：接收多个参数之后，输出时，分隔符号默认为空格，' '；  
`end='\n'`：输出行的末尾默认是换行符号 '\n'；  
`file=sys.stdout`：默认的输出对象是 sys.stdout（即，用户正在使用的屏幕）……

**[关于函数的理解总结:](https://github.com/hermanxie/the-craft-of-selfteaching-1/blob/master/Part.1.E.4.functions.ipynb)**
>* *你可以把函数当作一个产品，而你自己是这个产品的用户;*  
>* *既然你是产品的用户，你要养成好习惯，一定要亲自阅读产品说明书；*  
>* *调用函数的时候，注意可选位置参数的使用方法和关键字参数的默认值；*  
>* *函数定义部分，注意两个符号就行了，`[ ]` 和 `=`；*
>* *所有的函数都有返回值，即便它内部不指定返回值，也有一个默认返回值：`None`；* 
>* *另外，一定要耐心阅读该函数在使用的时候需要注意什么 —— 产品说明书的主要作用就在这里……*
---
### 4. 字符串

* **转换函数：**  
`ord()`: 把单个字符转换成码值  
`chr()`: 把整数（码值）转换成字符  
`\n`: 换行符号  `\t`:TAB键  
`input()`: 接收用户的键盘输入  
`len()`: 返回字符串的长度  
* **大小写：**  
**[这是一篇有用的文章：Truths programmers should know about case](https://www.b-list.org/weblog/2018/nov/26/case/)**  

  **大小写转换函数：**  
`str.upper()`: 大写；  
`str.lower()`: 小写；  
`str.swapcase()`: 大小写反转；  
`sre.casefold()`: 小写；  
`str.capitalize()`: 行首字母大写；  
`str.title()`: 词首字母大写。  

* **搜索、替换、删除**  
`str.count()`: 搜索字符串出现的**次数**（可以设定起始位置和结束位置参数）；  
`str.find()` 或者 `str.index()`: 从**字首**开始搜索字符串出现的**位置**（可以设定起始位置和结束位置参数）；  
`str.rfind()` 或者 `str.rindex()`: 从**末尾**开始搜索字符串出现的**位置**（可以设定起始位置和结束位置参数）；  
`str.startswith()`: 判断一字符串是否以某个*子字符串*为**起始字符**（可以设定起始位置和结束位置参数）；  
`str.endswith()`: 判断一个字符串是否以某个*子字符串*为**结束字符**（可以设定起始位置和结束位置参数）；  
`str.replace(old, new[, count])`: 用'new'替换'old'，并可以设置替换次数。  
`str.expandtabs()`: 把字符串中的 TAB（\t）替换成空格，默认是替换成 8 个空格 —— 当然你也可以指定究竟替换成几个空格。  
`str.strip([chars])`: 有2个功能——1.不带参数的情况下，去除一个字符串**首尾**（首字符串之前的空格，尾字符串之后的空格）的所有空白，包括空格、TAB、换行符等等；2.带参数的情况下，那么参数字符串中的所有字母都会被当做需要从**首尾**（首字符串和末尾的字符串）剔除的对象；  
`str.lstrip()`：删除左侧字符；`str.rstrip()`：删除右侧字符；  

* **拆分字符串**  

  `str.splitlines()`: 把每一行拆分出来作为列表（可以理解为拆分段落里的**行**）。  
  `str.split(sep=None, maxsplit=-1)`: 根据分隔符进行拆分，形成列表（可以理解为拆分每行内的**单个词**）。如果没有给 str.split() 传递参数，那么默认为用 None 分割（各种空白，比如，\t 和 \r 都被当作 None）;拆分次数默认为全部。  

* **拼接字符串**  
`str.join(_iterable_)`: `"str"`是指提供一个用来衔接的字符串；`"_iterable_"`是指被拼接的字符串**列表**。

* **字符串排版**  
`str.center(width[, fillchar])`:字符串居中对齐。  
`str.ljust(width)`: 字符串左对齐；  
`str.rjust(width)`: 字符串右对齐。

* **格式化字符串（插入字符串）：**  
`str.format(*args, **kwargs)`: `'str'`是指被插入的整体字符串；参数`(*args, **kwargs)`是被插入的字符串或表达式，需要用`{}`标示在`'str'`中的位置。  
`f-string`: 可以把任意数量的字符插入字符串中。

* **字符串的操作、函数、与Methods:**  
![**字符串的操作、函数、与Methods**](https://nbviewer.jupyter.org/github/hermanxie/the-craft-of-selfteaching-1/blob/master/images/string-concepts.png)

### 5. 数据容器

* 数据容器包括：**字符串**、由`range()`函数生成的**等差数列**、**列表**(list)、**元组**(tuple)、**集合**(set)、**字典**(dictionary)。  
这些容器，各有各的用处。其中又分为**可变容器**（Mutable）和**不可变容器**（Immutable）。可变的有**列表、集合、字典**；不可变的有**字符串**、range() 生成的**等差数列**、**元组**。集合，又分为 Set 和 Frozen Set；其中，**Set 是可变的**，**Frozen Set 是不可变的**。  
字符串、由 range() 函数生成的等差数列、列表、元组是**有序类型**（Sequence Type），而集合与字典是无序的。  
![数据容器分类](https://github.com/hermanxie/the-craft-of-selfteaching-1/raw/b20e3b092696cc0e098377345ffc56063768d7eb/images/python-containers-final.png)

* **可变序列的Methods**:  

  Name   |  Methods  
  -------|-------
  a.append()| 在末尾追加一个元素
  a.clear() | 清空序列
  a.copy() | 拷贝一个列表（在执行其他命令时，拷贝件和原件互不干扰
  a.extend(t) | 在末尾追加一个列表(t 代表另一个列表)
  a.insert(i, x)| 在某个索引位置插入一个元素(i代表位置，x代表字符)
  a.pop(i)| 删除某个位置的字符(i代表位置)，并可以将它赋予其他元素
  a.remove(x)| 删除字符，如果有多个同样的，删除第一个
  del a[i] | 删除某个位置的字符(i代表位置)
  a.reverse()| 逆序列表
  a.sort(key, reverse)| 从小到大排序，可以有参数

  ###### 注：a 代表一个列表；

* **列表操作符、函数、与Methods**
![](https://github.com/hermanxie/the-craft-of-selfteaching-1/raw/b20e3b092696cc0e098377345ffc56063768d7eb/images/list-concepts.png)