
## Python3 模块

模块是一个包含所有你定义的函数和变量的文件，其后缀名是.py。模块可以被别的程序引入，以使用该模块中的函数等功能。这也是使用 python 标准库的方法。  
模块实际就是函数库

## import 语句

引用模块的方法

```
import module1[, module2[,... moduleN]
```

当解释器遇到 import 语句，如果模块在当前的搜索路径就会被导入。  
相同模块只会导入一次,即使写了多次也会导用一次,不会影响效率

## 导入路径

```python
import sys # sys就是系统函数的标准库
sys.path # 环境变量
```

```
['', '/usr/lib/python38.zip', '/usr/lib/python3.8', '/usr/lib/python3.8/lib-dynload', '/usr/lib/python3.8/site-packages']
```

得到的就是python的路径,其中第一个空串代指当前目录  
如果是具体程序中空串将是实际路径,并且可能是多个路径(在pycharm中获得了这三个)  
```
'/mnt/g/Python/模块', '/mnt/g/Python', '/mnt/c/Program Files/JetBrains/PyCharm 2019.3/plugins/python/helpers/pycharm_display', 
```
python会在这些目录中依次寻找模块的  

## from … import 语句

这个方法将导入某些函数,而不是整个文件

```
from modname import fname1[, fname2[, ... fnameN]]
```

如果将函数名换成*表示导入全部

## __name__属性

一个模块被其他程序调用时会执行一次主程序,然后就不会执行了,如果想让他不执行这一次,可以使用`__name__`属性  
`__name__`属性的值为`__main__`时,表示程序是在当前程序执行,而不是被其他程序调用

和js一样`__ __`代表系统默认属性

## dir()函数

内置的函数 dir() 可以找到模块内定义的所有名称。以一个字符串列表的形式返回

```python
import sys
dir(sys) # 找出sys中导入的所有的名字
dir() # 没有参数是列出当前程序的所有名字
```

## 包

在sys.path中如果只存放py文件,看上去不太美观  
解决办法就是包(创建文件夹放py文件)  

包的导入方式如下:

```python
import sound.effects.echo # 导入
sound.effects.echo.fun()  # 使用
```

```python
from sound.effects import echo # 导入
echo.fun()                     # 使用
```

一般包文件夹中需要存在一个`__init__.py`文件(可以为空)
