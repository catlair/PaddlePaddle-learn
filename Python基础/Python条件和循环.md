
## 条件控制

条件控制的语法如下:

```
if 判断条件1:
    执行语句1……
elif 判断条件2:
    执行语句2……
elif 判断条件3:
    执行语句3……
else:
    执行语句4……
```

习惯了c语言的语法,这缩进语法看着真的很难受

## while循环

```
while 判断条件(condition)：
    执行语句(statements)……
```

同样的continue 用于跳过该次循环，break 则是用于退出循环

### while...elif...

```
while <expr>:
    <statement(s)>
else:
    <additional_statement(s)>
```

while的条件不满足时执行else

## for循环

for循环和while循环类似

for循环可以遍历各种数据类型(用法同js的for...in)

```python
for letter in 'Runoob':
    print('当前字母为 :', letter)

```

## pass语句

??? 这个不知道干嘛用的,仅仅占一行而已?