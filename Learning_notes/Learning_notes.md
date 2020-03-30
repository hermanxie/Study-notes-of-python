# 编程学习笔记
---
* **有用的必读内容：** 

  [**1. Python代码样式指南**](https://www.python.org/dev/peps/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds)  
  [**2. Python 说明书**](https://docs.python.org/zh-cn/3/)  
  >* [**Python 教程**](https://docs.python.org/zh-cn/3/tutorial/index.html)  
  >* [**Python 标准库**](https://docs.python.org/zh-cn/3/library/index.html)
  >* [**Python 代码仓库**](https://github.com/python/)
  >* [**Python Demo 程序**](https://github.com/python/cpython/tree/master/Tools/demo)  

  **3. Python 学习书**  
  * [**Free books by Allen B. Downey**](https://greenteapress.com/wp/think-dsp/)
    * [**ThinkPython(Github)**](https://github.com/AllenDowney/ThinkPython2)   
    * [**ThinkPython(htm)**](http://greenteapress.com/thinkpython2/html/index.html)  
  * [**Python for Everybody**](https://www.py4e.com/book)
    * [**Python for Everybody:html**](https://eng.libretexts.org/Bookshelves/Computer_Science/Book%3A_Python_for_Everybody_(Severance))
    * [**视频bilibili**](https://www.bilibili.com/video/BV16b411n7U4?p=1)
    * [**视频coursera**](https://www.coursera.org/learn/python?specialization=python#syllabus)
  * [**A Bite of Python**](https://python.swaroopch.com/control_flow.html)  
  * [**Dive Into Pyton**](https://linux.die.net/diveintopython/html/)
  * [**Python 练习题**](https://pythonbasics.org/exercises/)
  * [**Guide to Python**](https://docs.python-guide.org/)
  * [**更多学习资料**](https://github.com/hermanxie/the-craft-of-selfteaching-1/blob/master/S.whats-next.ipynb)
---
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
  * **注：** 因为`**`比-拥有更高的优先级，所以 `-3**2`会被解释成 `-(3**2)` ,因此结果是`-9`，为了避免这个并且结果得到 `9`，可以用这个句式 `(-3)**2`。

  **完整的操作符优先级列表，参见 [官方文档](https://docs.python.org/zh-cn/3/reference/expressions.html#operator-precedence)。**

* **布尔值操作符：**  
  `与、或、非：and、or、not`它们之中，优先级最低的是或 or，然后是与 and, 优先级最高的是非 not。

  **操作符优先级：** 数值计算的操作符优先级最高，其次是逻辑操作符，布尔值的操作符优先级最低。

* **值的类型及转换：**  

  Name | Method  
  ---- | :----:  
  `int()、float()` | 将字符串转换为数字用  
  `str()` | 将数字转换成字符串用  
  `float()` | 将整数转换成浮点数字用  
  `int()` | 将浮点数字转换成整数用  
  `type()` | 查看某个值属于什么类型  


* **字符串的三种操作：**

1. 拼接：`+` 和 `' '`（后者是空格）
2. 拷贝：`*`
3. 逻辑运算：`in、not in`；以及，`<、<=、>、>=、!=、==`
4. 转义符：`\`; 如果想要显示`\`,则在引号前加 `r` ，参考[说明书](https://docs.python.org/zh-cn/3/tutorial/introduction.html)。
5. 需要换行时：用`'''   '''`或`"""   """`来包含字符串。

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

* **函数定义**：函数是一个完整的程序，包含 **输入（参数传递）、处理（运行特定代码）、输出（返回值）** 三个部分。  
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
>* *理解函数输入输出的基本结构；*
>* *注意函数的取名，不要和关键字重名，关键字查询的函数：keyword.iskeyword('函数名')；*

* **关于参数：**  
**参数：** 简单理解，参数就是一个**值**，是传递给**函数**或**Methon**的值。

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
![数据容器分类](https://github.com/hermanxie/Study-notes-of-python/blob/master/images/python-containers-final.png)

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
![](https://github.com/hermanxie/Study-notes-of-python/blob/master/images/list-concepts.png)

* **集合(set)**  
集合（Set）这个容器类型与列表不同的地方在于，首先它**不包含重合元素**，其次它是无序的；进而，集合又分为两种，Set，可变的，Frozen Set，不可变的。  

  **集合的操作符有：**

  操作符 | 意义 | Methods | 解释  
  ------ | ----- | ----- | -----  
    \|   | 并集 | set1.union(*set2) | 一个集合与另一个集合合并  
   & | 交集 | set1.intersection(*set2) | 两个集合相交，返回其中相同的元素  
   - | 差集 | set1.difference(*set2) | 第1个集合减去两个集合中相同的，返回第1个集合中剩下的元素  
    |  | set2.difference(*set1) | 第2个集合减去两个集合中相同的，返回第2个集合中剩下的元素 
    ^ | 对称差集 | set1.symmetric_difference(*set2) | 把第一个和第二和集合中相同的都减去，返回两个集合中剩下的元素

    注：并集、交集、差集都可以接收多个集合作为参数(*set2)，但对称差集只能接收一个参数。

  **逻辑运算:**  
两个集合之间可以进行逻辑比较，返回布尔值。  
`set == other`  
True: set 与 other 相同  
`set != other `   
True: set 与 other 不同  
`isdisjoint(other)`  
True: set 与 other 非重合；即，set & other == None  
`issubset(other)，set <= other `   
True: set 是 other 的子集  
`set < other`  
True: set 是 other 的真子集，相当于 set <= other && set != other  
`issuperset(other)，set >= other `   
True: set 是 other 的超集  
`set > other`  
True: set 是 other 的真超集，相当于 set >= other && set != other  

  **更新:**  
对于集合，有以下更新它自身的 Method：  
`add(elem)`  
把 elem 加入集合  
`remove(elem)`  
从集合中删除 elem；如果集合中不包含该 elem，会产生 KeyError 错误。  
`discard(elem)`  
如果该元素存在于集合中，删除它。  
`pop(elem)`  
从集合中删除 elem，并返回 elem 的值，针对空集合做此操作会产生 KeyError 错误。  
`clear()`  
从集合中删除所有元素。  
`set.update(*others)，`相当于 set |= other | ...  
更新 set, 加入 others 中的所有元素；  
`set.intersection_update(*others)`，相当于 set &= other & ...  
更新 set, 保留同时存在于 set 和所有 others 之中的元素；  
`set.difference_update(*others)`，相当于 set -= other | ...  
更新 set, 删除所有在 others 中存在的元素；  
`set.symmetric_difference_update(other)`，相当于 set ^= other  
更新 set, 只保留存在于 set 或 other 中的元素，但不保留同时存在于 set 和 other 中的元素；注意，该 Method 只接收一个参数。


## 6. 文件
* **创建文件**  
`open(file, mode='r')`: Python创建文件使用的内建函数。  

  第二个参数，mode的默认值是'r'，可用的mode有以下几种：  

  参数字符 | 意义  
  ---- | ----  
  'r' | 只读模式
  'w' | 写入模式（重建）
  'x' | 排他模式——如果文件已存在则打开失败
  'a' | 追加模式——在已有文件末尾追加
  'b' | 二进制文件模式
  't' | 文本文件模式（默认）
  '+' | 读写模式（更新）

* **删除、读写文件的方法**  

  函数 | 使用解释  
  -----| ----  
  os.remove(file.name) : | 使用前，必须先调用 os 模块
  file.write() | 创建文件之后，可以用来把数据写入文件
  file.writelines() | 把一个列表写入到一个文件中
  file.read() | 创建文件之后，可以用来读取文件  
  file.readline() | 有很多行时，可以用这个Method，每次调用都会返回文件的新一行
  file.readlines() | 将文件作为一个列表返回，列表中的每个元素对应着文件中的每一行。

## 7. 流程控制

* **`while`循环**：后面跟随的是一个**赋值表达式**，根据赋值表达式的**真假**来决定执行还是终止。  
* **`for` 循环**：后面跟随的是一个**序列**（字符串、元组或列表）。  
* **`if、elif` 语句**：后面跟随的是一个**赋值表达式**；else 后面跟随的是一个**句体**。  

## 8. 函数命名

* 为一个函数**取名的原则**：
  * 避免重名
  * 不要嫌麻烦，尽可能描述清晰
  * 取一个化名
  * 避免变量和函数同名

* **lambda** （匿名函数）:  
  * lambda使用方式：lambda <参数列表> : <表达式>。
    >示例：`lambda x, y : x + y`

  **总结：**  
  * 注意函数化名的使用，**带参数**与**不带参数**，代表的意思是不一样的。比如：`f = function_name` 这是函数化名； `f = function_name(<参数>)` 这是把 `function_name(<参数>)`这个函数的 **返回值（这个返回值不一定是一个具体的数值，也可能是另一个函数）** 赋给变量 `f`。

## 9. 递归函数
* 递归函数遵循三个原则：  
  >1.根据定义，递归函数必须在内部调用自己；  
2.必须设定一个退出条件；  
3.递归过程中必须能够逐步达到退出条件……

* [**普林斯顿大学的一个网页，有很多递归的例子**](https://introcs.cs.princeton.edu/java/23recursion/)  

## 10. 函数的说明文档
* 书写Docstring的规范：  
  >1.无论是单行还是多行的 Docstring，一概使用三个双引号括起；  
2.在 Docstring 内部，文字开始之前，以及文字结束之后，都不要有空行；  
3.多行 Docstring，第一行是概要，随后空一行，再写其它部分；  
4.完善的 Docstring，应该概括清楚以下内容：参数、返回值、可能触发的错误类型、可能的副作用，以及函数的使用限制等等；  
5.每个参数的说明都使用单独的一行……

## 11. Class  
关于Class需要注意的：  
  >在 `Class` 的代码中，如果定义了 `__init__()` 函数，那么系统就会将它当作“ `Instance` 在被创建后初始化的函数”。这个函数名称是**强制指定**的，初始化函数**必须使用这个名称**；注意 `init` 两端各有两个下划线 `_`。