# 第十讲-函数、模块与lambda表达式
## 定义一个普通函数
```python
def 函数名([形参1, 形参2, ... , 形参n]):
  函数体
```
## 把 Python 程序按 C 的方式组装起来
```python
def 子函数():
  函数体
def main():
  子函数
  return
```
## 函数返回多个值
本质上是返回元组。
```python
def f(x,y):
    return x+y,x*y,x/y
print(f(2,4))
```
返回
```python
(6, 8, 0.5)
```
## 空函数和空返回值
函数定义以后函数体中必须写语句。

如果函数什么都不做，写 `pass` 占位。

如果函数没有返回值，其返回值将为 `None`。
## 调用函数时不加括号会发生什么
```python
>>> def f():
	print('AAA')
>>> f
<function f at 0x0000027FAFC43950> # 显示了 f 是一个函数，但是 f() 并未被调用。
>>> f()
AAA   # 正确的输出
```
## 变长参数
```python
>>> x,y = 1,2,3,4,5
Traceback (most recent call last):
  File "<pyshell#5>", line 1, in <module>
    x,y = 1,2,3,4,5
ValueError: too many values to unpack (expected 2)
>>> x,*y = 1,2,3,4,5     # 加星号的就是变长参数
>>> x
1
>>> y
[2, 3, 4, 5]
>>> x,*y,z = 1,2,3,4,5
>>> x
1
>>> y
[2, 3, 4]
>>> z
5
# 按位置先分配元素，剩余的全部交给变长参数。
```
一个元组中最多可以有一个变长参数。

可以用变长参数的方法给函数传参。

例程如下：
```python
>>> def f(x,*y):
	print("x=",x,"y=",y)	
>>> f(2,3,4,5)
x= 2 y= (3, 4, 5)
```
但是**在函数形参表当中，只有最后一个形参**可以加`*`变为变长参数，不能像上面 `x, *y, z` 那样使用。
## lambda 表达式
lambda 表达式以
```python
标识符 = lambda 形参表: 表达式
```
的形式构成。

上述赋值语句的右值即为 lambda 表达式，作为“匿名函数”，可以不命名。

但为了调用方便起见，将其赋值给一个标识符，之后就可以以

```python
标识符(形参表)
```
的形式调用表达式。

```python
x,y=eval(input('输入点的坐标'))
distance=lambda x,y:x**2+y**2
print('点到原点的距离=√',distance(x,y),sep='')
```
### 给参数设置默认值
lambda 表达式也可以在声明时对形参赋值。

这样，当缺省形参时，就代入所赋值的默认值。

lambda 表达式可以使用变长形参：
```python
>>> f=lambda x,*y:print(x,y)
>>> f(2,3,4,5,6)
2 (3, 4, 5, 6)
```
老师上课讲错了。

## lambda 表达式可以作为列表、元组的分量
例程如下：
```python
import math
x,y=eval(input('输入点的坐标'))
distance=[lambda x,y:x**2+y**2, lambda x,y:math.sqrt(x**2+y**2)]
print('点到原点的距离=√',distance[0](x,y),sep='') # 调用了索引为 0 的表达式
print('点到原点的距离=',distance[1](x,y),sep='') # 调用了索引为 1 的表达式

# 输出如下
输入点的坐标3,4
点到原点的距离=√25
点到原点的距离=5.0
```
## 函数的递归
调用自身的函数就构成直接递归。

调用别的函数，那个函数再调用本函数，就构成间接递归。

递归例程：
```python
def f(n):
    if n<=1:
        return 1
    else:
        return n*f(n-1)
print(f(3))
```
输出 6。

if 语句中的 n<=1 就是递归出口条件，下面的选择支没有出现 f 函数的调用，可以使递归停止。
## 全局变量
函数外定义的变量就是全局变量。

如果函数体中，如果要对全局变量重新赋值，可以使用 global 关键字。

```python
>>> GlobalVar = 3
>>> def f(n):
	GlobalVar = n	
>>> f(100)
>>> GlobalVar
3

# 这里可以发现，函数体不能修改全局变量。

>>> def f(n):
	global GlobalVar # 在此声明全局变量，表明这里的 GlobalVar 就是函数体外的那个全局变量 GlobalVar
	GlobalVar = n
	
>>> f(100)
>>> GlobalVar
100

# 这里可以看到全局变量 GlobalVar 被改变。
```
### nonlocal 关键字
可以指明函数体中出现的变量不是该函数体的局部变量。

这时，解释器就会将其解释为外层函数的变量。
