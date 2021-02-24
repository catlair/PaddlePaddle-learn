
from typing import Dict

##  变量赋值

除了正常的赋值,python还支持以下方式

```python
a = b = c = 1
```

```python
a, b, c = 1, 2, 3
```

## 数据类型

- Numbers 数字
- String 字符串
- List 列表
- Tuple 元组
- Set 集合
- Dictionary 字典 

- ***不可变数据（3 个）：*** Number（数字）、String（字符串）、Tuple（元组）；
- ***可变数据（3 个）：*** List（列表）、Dictionary（字典）、Set（集合）。

### 数字类型

- int 整形
- long 长整型

  长整型只存在2.x之中,2.2之后int会自动转换成long,3.x没有long  
  例如: 51924361L  

- float 浮点型
- complex 复数  

    例如: 9.322e-36j

### 字符串类型

字符串类型的索引和javascript的一样  
例如: abcd  
正数: a是第0个字符  
倒数: d是第-1个字符

```python
print (str)         # 输出完整字符串
print (str[0])      # 输出字符串中的第一个字符
print (str[2:5])    # 输出字符串中第三个至第六个之间的字符串
print (str[2:])     # 输出从第三个字符开始的字符串
print (str * 2)     # 输出字符串两次
print (str + "TEST" ) # 输出连接的字符串
```

### 列表

和数组似乎没有差别,支持每项不同类型,截取和String类型一样

```python
a = [1,2,3]
```

### 元组

类似列表但是只读不可写

```python
a = (1,2,3)
```

### 集合

如同名字,集合中相同的元素只会留下一个

```python
a = set('abracadabra')
# a = {'d', 'r', 'c', 'a', 'b'}
```

### 字典

很像JavaScript的对象(不能用`.`运算符,任何不可变数据都可以做key)

```python
dict = {}
dict['one'] = "This is one"
dict[2] = "This is two"

tinydict = {'name': 'john', 'code': 6734, 'dept': 'sales'}

print(dict['one'])  # 输出键为'one' 的值
print(dict[2])  # 输出键为 2 的值
print(tinydict['name'])  # 输出键为name的value
print(tinydict.keys())  # 输出所有键
print(tinydict.values())  # 输出所有值
```

## 运算符

基本运算符不介绍了(和javascript相似)

没有++和--运算符
有+和-(正负运算符)

```python
2 ** 2 == 4 # 幂计算
9 // 2 == 4 # 取商的整数,向下取整
```

### 逻辑运算

python的逻辑运算符不是&&,||和!  
取而代之的是and,or和not

### 成员运算符

in / not in
作用如其名,可用于包括字符串,列表,元组或字典

```python
    a  = {'name': 'xiaowang'}
    'name' in a
```

### 身份运算符

is / is not
x is y, 类似 id(x) == id(y) 
作用说是比较地址,但是用js去思考我是真的没看懂这is底层是什么样的?