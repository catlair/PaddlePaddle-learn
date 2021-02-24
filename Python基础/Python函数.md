
## 定义一个函数

def关键词开头,后接函数名和小括号,命名规划和c语言一致

```
def 函数名（参数列表）:
    函数体
```

***实例***
```python
def area(width, height):
    return width * height
area(12,2)
# 24
```

## 参数传递

由于python中万物皆对象,不能说值传递还是引用传递，我们应该说传不可变对象和传可变对象。
这和c,javascript很大的差别

### 必需参数

参数的数量和顺序需要必须正确

### 关键字参数

关键字参数可以避免参数的顺序出错

```python
#可写函数说明
def printinfo( name, age ):
   "打印任何传入的字符串"
   print ("名字: ", name)
   print ("年龄: ", age)
   return

#调用printinfo函数
printinfo( age=50, name="runoob" )
```

### 默认参数

无话可说

### 不定长参数

```python
def printinfo( arg1, *vartuple ):
   "打印任何传入的参数"
   print ("输出: ")
   print (arg1)
   print (vartuple)
 
# 调用printinfo 函数
printinfo( 70, 60, 50 )
```

实际上和ES6的剩余参数相似,只是多余的参数用元组保存

***还有另一种形式***

```python
def printinfo( arg1, **vardict ):
   "打印任何传入的参数"
   print ("输出: ")
   print (arg1)
   print (vardict)
 
# 调用printinfo 函数
printinfo(1, a=2,b=3)
```

导入形式不是元组而是字典了

还能单独一个*

```python
def f(a,b,*,c):
    return a+b+c
```

暂时不知这有什么用,传参时c还必须用关键词参数

## 匿名函数

语法:

```
lambda [arg1 [,arg2,.....argn]]:expression
```

例子:

```python
# 可写函数说明
sum = lambda arg1, arg2: arg1 + arg2
 
# 调用sum函数
print ("相加后的值为 : ", sum( 10, 20 ))
print ("相加后的值为 : ", sum( 20, 20 ))
```

## 强制位置参数

python3.8中使用/设置强制位置参数
下面例子中a,b必须用对应位置的参数

```python
def f(a, b, /, c, d, *, e, f):
    print(a, b, c, d, e, f)
f(10, 20, 30, d=40, e=50, f=60)       #正确
f(10, b=20, c=30, d=40, e=50, f=60)   # b 不能使用关键字参数的形式
f(10, 20, 30, 40, 50, f=60)           # e 必须使用关键字参数的形式
```

## return

不带参数值的return语句返回None