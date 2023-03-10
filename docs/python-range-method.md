# 了解 Python range()方法

> 原文：<https://www.askpython.com/python/built-in-methods/python-range-method>

## 介绍

今天在本教程中，我们将讨论 Python range()方法。

在 Python 的 **[for 循环](https://www.askpython.com/python/python-for-loop)** 中广泛使用了`range()`方法，用于遍历或迭代任何序列。

## Python range()方法

与其说是一个函数，`range()`实际上是一个不可变的序列类型。它返回 range 类型的数字序列。

使用 Python `range()`函数的语法如下。

```py
range(start, stop[, step])

```

这里，

*   **start(可选)**是序列生成开始的起始编号。它被包括在序列中，并且如果没有提及，则默认设置为 0，
*   **stop** 是序列生成停止之前的数字(不含)，
*   **step(可选)**是生成序列时该函数将要跳转的步骤。如果没有提供，则默认情况下认为是 1。

## 在 Python 中使用 range()方法

现在让我们看看实际使用 Python `range()`方法的各种方式。

### 1.只有一个参数

两个参数`step`和`start`是可选的，默认分别设置为 **1** 和 **0** 。但是对于序列生成，stop 参数是强制的。

仅提及停止时，`range()`功能创建一个从 **0** 到**(停止-1)** 的序列，步长为 **1** 。看看下面的例子。

```py
#range() with one parameter

print("Type of object returned by range: ", type(range(5)))

list1 = list(range(5))
print("sequence generated by range() with 1 parameter: ", list1)

```

**输出**:

```py
Type of object returned by range:  <class 'range'>
sequence generated by range() with 1 parameter:  [0, 1, 2, 3, 4]

```

正如我们所见，该方法生成的序列类型是类`range`的成员。根据需要，对`range()`输出进行类型转换会给出一个列表，其中包含值 **0** 到 **4(5-1)** 以及步长 **1** 。

### 2.有两个参数

同样，我们可以使用带有两个参数的`range()`方法。在这种情况下，**步**参数默认设置为 **1** 。

这个例子很容易解释。

```py
#range() with two parameter

list1 = list(range(3,7))
print("sequence generated by range() with 2 parameter: ", list1)

```

**输出**:

```py
sequence generated by range() with 2 parameter:  [3, 4, 5, 6]

```

从输出可以清楚地看出`step`被设置为 **0** 。

### 3.有三个参数

当提到所有参数时，`range()`函数产生一个从**开始**到**停止-1** 的序列。起始值之后的每个元素的值计算为前一个元素和**步骤**的和。

下面的例子很好地说明了这一事实。

```py
#range() with three parameter

list1 = list(range(3,20,3))
print("sequence generated by range() with 3 parameter: ", list1)

```

**输出**:

```py
sequence generated by range() with 3 parameter:  [3, 6, 9, 12, 15, 18]

```

从输出可以清楚地看出，序列是用范围 **3** 到 **19(20-1)** 内的值生成的。对于最后一个元素，仅仅因为 **18+3=21** 超过了停止点(20 ),序列生成在 **18 终止。**

## 在 Python 中对 for 循环使用 range()方法

正如我们前面提到的，`range()`在`for`循环结构中被广泛使用。让我们看一个简单的例子。

```py
#range() with for loop

for i in range(1,5):
    for j in range(1,i+1):
        print(j , end="")
    print()

```

**输出**:

```py
1
12
123
1234

```

在上面的代码中，我们试图打印一个模式，其中每一行都有由内循环中的`range(1,i+1)`方法返回的序列中的数字。对于外循环的最后一次迭代( **i=4** )，内循环从 *1* 到 **(4+1)-1 =4** 迭代 j 的值。

因此，输出是合理的。

## 结论

所以在本教程中，我们理解了 Python 中`range()`方法的概念。如有任何进一步的问题，欢迎使用下面的评论。

## 参考

*   [range()](https://docs.python.org/3/library/functions.html#func-range)–Python 文档，
*   python range()–日志开发帖子，
*   [为什么 range(start，end)不包括 end？](https://stackoverflow.com/questions/4504662/why-does-rangestart-end-not-include-end)–堆栈溢出问题。