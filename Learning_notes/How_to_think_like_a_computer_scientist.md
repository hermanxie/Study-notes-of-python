# [Think Python:How to think like a computer scientist](http://greenteapress.com/thinkpython2/html/index.html)

## 第一章  函数的一些基本概念
### 1.1 **What is a program?**

A program is a **sequence** of **instructions** that specifies how to **perform** a **computation**.

* **一个重要的概念**：  
    >程序是：**指定**如何**执行运算**的**指令序列**。  
【首先，程序就是一个**指令序列**，这个指令序列其实是一个**运算方法**，是可以被用来**指定执行**的。】

    你曾经用过的每一个程序，不管它有多复杂，都是由类似这样的指令组成的。因此，您可以将编程看作是**将一个大而复杂的任务分解成越来越小的子任务的过程**，直到这些子任务**足够简单**，可以**使用**这些**基本指令**之一来执行为止。  

    程序的基本框架：  
**输入**:从键盘、文件、网络或其他设备获取数据。  
**输出**: 在屏幕上显示数据，将数据保存到文件中，通过网络发送数据，等等。  
**数学**: 执行基本的数学运算，如加法和乘法。  
**条件执行**: 检查某些条件并运行适当的代码。  
**重复**: 重复地做一些动作，通常会有一些变化。

### 1.2 关于自然语言与形式语言

* **形式语言**：是人们为特定程序而设计的语言。  
* **程序语言**：是指设计用来表达计算的形式语言。  
* **解析**：当你用英语读一个句子或用形式语言读一个语句时，你必须弄清楚它的结构(尽管在自然语言中你是下意识地这么做的)。这个过程称为解析。

* 自然语言与形式语言的**区别**：  
**歧义**：  
自然语言中充满了歧义，人们通过语境线索和其他信息进行处理。形式语言被设计成几乎或完全无二义性，这意味着无论上下文如何，任何语句都只有一种含义。  
**冗余**:  
为了弥补歧义和减少误解，自然语言使用了大量的冗余。因此，它们常常很冗长。  形式语言不那么冗余，而且更简洁。  
**文字**：  
自然语言充满了习语和隐喻。形式语言则言出必行，必须表达完全准确。   
**解读**：  
正式语言比自然语言更密集，因此阅读它们需要更长的时间。此外，结构也很重要，所以从上到下、从左到右阅读并不总是最好的。相反，要学会**在头脑中解析程序**，**识别标记**并**解释结构**。最后，细节很重要。在自然语言中，拼写和标点符号上的小错误是可以避免的，但在正式语言中，这些错误可能会造成很大的差异。

### 1.3 调试  

程序员会犯错。出于古怪的原因，**编程错误被称为bug**，**跟踪它们的过程**被称为**调试**。
>【调试过程就像公司管理，把计算机看作你的员工，你要和它相处好，利用好它的长处，不要由它而引起自己的情绪，破坏自己的工作。】  

学习调试可能令人沮丧，但它是一种宝贵的技能，对于编程以外的许多活动都很有用。在每一章的结尾处都有一节，就像这一节一样，提供了我的调试建议。我希望他们能帮上忙!

## 第二章 变量、表达式、语句

变量：是指一个引用值的名称。  
变量名可以任意长。它们可以包含字母和数字，但不能以数字开头。使用大写字母是合法的，但通常只对变量名使用小写字母。**关键字**不能被用作变量名。  

**Python 3 has these keywords:**  
keywords | keywords | keywords | keywords | keywords
--- | --- | --- | --- | ---
False | class | finally | is | return
None | continue | for | lambda | try
True | def | from | nonlocal | while
and | del | global | not | with
as | elif | if | or | yield
assert | else | import | pass
break | except | in | raise

**2.1 表达式和语句**  
* **表达式**是**值、变量和操作符**的组合。一个**值**本身被认为是一个表达式，所以也是一个变量。  
* **语句**是具有效果的**代码单元**，如创建变量或显示值。比如`n = 17`、`print(n)`。  

**2.2 脚本模式**  
* **概念**：解释器直接运行的简短代码是交互模式；把长的代码保存为一个可供解释器读取的文件，就是脚本模式。  

* 解释器是运行语句（或代码块）、脚本；编译器是用来写脚本的，脚本里面包含语句和表达式。

**2.3 运算的优先级(PEMDAS)**  

Name | Sign | Precedence
--- | --- | ---
Parentheses(圆括号) | `()`  | Highest
Exponentiation(求幂) |  `**`  | Next Highest
Multiplication(乘法)、Division(除法) | `*` `/` | Higher
Addition(加法)、Subtraction(减法) | `+` `-` | Last

注：具有相同优先级的操作符从左到右计算

**2.4 关于取名和解释**
* 好的变量名可以减少注释的需要，但是长名称会使复杂的表达式难于阅读，因此需要权衡。

**2.5 调试**  

程序存在的三种错误：
* **语法错误(Syntax error):** 
语法是指程序的**结构**和与**结构有关的规则**。
* **运行错误(Runtime error):**
是指程序已经开始运行，直到结束才提示，这也叫**发生异常(Exception)**。
* **语义错误(Semantic error)**
如果你的程序有语义错误，程序在运行过程中不会有任何提示，但运行的结果不是你想要的。

## 第三章 函数(Functions)

* 函数的定义：是指在编程语境中，**执行运算**的**语句序列**。
* 模块的定义：是指包含**一组相关函数**的文件。

* **形式参数和实际参数**：  
    >* 形式参数：在函数内部，被分配给变量的参数。通俗理解是给参数取个名而已。作为参数传递的**变量的名称**与形式参数的名称没有任何关系。  
    >* 每个形参都指向与它**对应的**实参**相同的值**。
    ```
    def print_twice(bruce):    # 'bruce'就是一个形式参数，仅仅是这个函数内部参数的代名。
    print(bruce)
    print(bruce)

    michael = 'Eric, the half a bee.'
    print_twice(michael)          # 变量‘michael'是实际参数，可以是任意名称，比如'x'、'y'…… 
    print_twice('Spam '*4)        # 实际参数可以是函数、变量、数值、表达式等
    print_twice(math.cos(math.pi))
    ```

* 函数内的变量是局部变量，它只在函数内部执行运算。

* 当函数内部有2个参数，第一个参数是一个函数`f`时，第二参数可以作为函数`f`的值：  
    ```
    def do_twice(func, a):
        func(a)
        func(a)
    # 运行这个函数
    do_twice(print, 'Hello world!')    # print 代表任意一个可执行的函数

    # 返回的结果是：
    Hello world!
    Hello world!
    ```
---
* **本章的总结：**
1. 函数取名的注意事项：  
    * 避免重名  
    * 不要嫌麻烦，尽可能描述清晰
    * 取一个化名
    * 避免变量和函数同名
    * 避免使用关键字作为函数名
2. 对函数内部的参数要理解：形参与实参的概念及运用要理解。

---
## 第四章 案例学习

* 将一段代码块装进函数中，叫做**封装(Encapsulation)**。

* 添加参数给一个函数，使函数更加一般化，叫做**泛化(Generalization)**。

* 函数如何使用的信息说明，叫做**代码接口(Interface design)**。

* 重新安排一个程序改进接口，并使代码重新使用更容易，这个过程叫**代码重构(Refactoring)**。

* **开发计划：** 是编写程序的过程。
    >第一步，编写一个没有函数定义的**小程序**。  
    第二步，让你的程序运行，识别它连贯的部分，给它**取个名字并封装**在一个函数中。  
    第三步，通过**添加适当的形式参数**来泛化函数。  
    第四步，重复1-3步，直到有了**一组运算函数**。为了避免重复输入和测试，这些工作通过拷贝和粘贴原有运行代码来完成。  
    第五步，寻找通过**重构**去优化程序的机会。比如，如果在不同的地方有类似的代码，可以考虑将它分解为一个适当的通用函数。

## 第五章 条件语句和循环语句

概念名 | 概念解释 | 概念语句 | 应用  
--- | --- | --- | ---
整除和余数运算符 | 四舍五入为整数；返回剩下得余数  | `//` `%` | 余数运算可以用来**抽取**一组数字**最右边的数**。比如，`x % 10` 可以得到最右边一位数；`x % 100` 可以得到右边的两位数……
布尔运算 | 是一个要么为真要么为假得表达式 | `==` `!=` `>` `<` `>=` `<=` | 判断真假，及表示关系运算
逻辑运算 | 严格来说，逻辑运算的运算体应该是布尔表达式；任何非零数字都解释为真 | `and` `or` `not` |  
条件执行 |   | `if` | 
复合语句 | 由标题和缩进体组成 |   | 
选择执行 | 有两种可能性，条件决定哪一种运行;替代条件也叫做**分支** | `if……` \n `else……` | 
链式条件 | 超过两个分支以上的表达条件 | `elif` | 链式条件的数量不限 （见注释1）
嵌入条件 | 一个条件可以被嵌套在另一个条件中 | 在`else`后面可以再增加 `if` 语句  | 嵌入条件不是很容易读，尽量避免使用（注释2）
递归 | 一个函数调用调用自身，并且执行的这个过程叫递归 |  | 见注释3

```
注释1： 
if x < y:
    print('x is less than y')
elif x > y:
    print('x is greater than y')
elif ……         # 不限数量
else:
    print('x and y are equal')

注释2：
if x == y:
    print('x and y are equal')
else:
    if x < y:
        print('x is less than y')
    else:
        print('x is greater than y')

注释3：
def countdown(n):
    if n <= 0:
        print('Blastoff!')
    else:
        print(n)
        countdown(n-1)
```
**if语句的几种表达形式**：  

第一种：
```
if ……
```
第二种：
```
if ……：
    print(……)
else:
    print(……)
```
第三种：
```
if ……：
    print(……)
elif ……：
    print(……)
elif ……：
    print(……)
……
```
第四种：
```
if ……：
    print(……)
elif ……：
    print(……)
……
else:
    print(……)
```

## 第六章 有效的函数

增量开发：增量开发的目标是通过一次只添加和测试少量代码来避免长时间的调试会话。
* 增量开发的关键方法：  
1. 从一个工作程序开始，做一些**小的增量更改**。在任何时候，如果出现错误，你应该**知道它在哪里**并有解决方案。
2. 使用变量来保存中间值，以便您可以**显示和检查**它们。
3. 一旦程序开始工作，您可能希望删除一些**scaffoldiing**，或者将多个语句**合并**到复合表达式中，但只有在它不会使程序难于阅读的情况下才会这样做。

>如果一个函数不运行，有**三种可能性**：  
    1. 违反了先决条件；  
    2. 违反了后置条件；  
    3. 返回值或使用它的方式有问题。

pass
