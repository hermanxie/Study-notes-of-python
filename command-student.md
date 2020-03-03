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
  `与、或、非：and、or、not`

  它们之中，优先级最低的是或 or，然后是与 and, 优先级最高的是非 not。

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

1. `mkdir`: 新建文件
2. `ren`:文件重命名

### 3. 常用函数  
>**[python常需查看的标准库](https://docs.python.org/zh-cn/3/library/index.html)**  
**[python内置函数说明书](https://docs.python.org/zh-cn/3/library/functions.html#divmod)**  
**[python内置类型说明书](https://docs.python.org/zh-cn/3/library/stdtypes.html)**  

* **f-string: 把变量或者表达式的值插入字符串中。**

举例：
```
name = 'Ann'
age = '22'
print(f'{name} is {age} years old.')  花括号 {} 括起来的部分是表达式
```

* **print:**


>`print(*object, sep=' ', end='\n', file=sys.stdout, flush=False)`  
`sep=' '`：接收多个参数之后，输出时，分隔符号默认为空格，' '；  
`end='\n'`：输出行的末尾默认是换行符号 '\n'；  
`file=sys.stdout`：默认的输出对象是 sys.stdout（即，用户正在使用的屏幕）……

**[关于函数的理解总结:](https://github.com/hermanxie/the-craft-of-selfteaching-1/blob/master/Part.1.E.4.functions.ipynb)**
>* *你可以把函数当作一个产品，而你自己是这个产品的用户;*  
>* *既然你是产品的用户，你要养成好习惯，一定要亲自阅读产品说明书；*  
>* *调用函数的时候，注意可选位置参数的使用方法和关键字参数的默认值；*  
>* *函数定义部分，注意两个符号就行了，`[ ]` 和 `=`；  *
>* *所有的函数都有返回值，即便它内部不指定返回值，也有一个默认返回值：`None`； * 
>* *另外，一定要耐心阅读该函数在使用的时候需要注意什么 —— 产品说明书的主要作用就在这里……*

### 4. 字符串

* **转换函数：**  
`ord()`: 把单个字符转换成码值  
`chr()`: 把整数（码值）转换成字符  
`\n`: 换行符号  `\t`:TAB键  
`input()`: 接收用户的键盘输入  
`len()`: 返回字符串的长度  
* **大小写：**  
**[这是一篇有用的文章：Truths programmers should know about case](https://www.b-list.org/weblog/2018/nov/26/case/)**  

