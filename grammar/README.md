## 基础语法

### 数据类型

+ 五种标准数据类型：`Numbers`、`String`、`List`、`Tuple`、`Dictionary`

```python
num = 123 # 数字
text = 'Hello World' # 字符串
arr = [num, text, 321, [3, 4]] # 列表，列表项可以为任意类型，且可以嵌套
_tuple = (num, text, 321, (3, 4)) # 元组，与列表的区别在于元组项不可被改变
dictionary = {'a': 1, 'b': 2} # 字典，字典类型为键值对型对象
```

+ 元组项不可被改变，例：
```python
num = 123
numTuples = (num, 456)
print(numTuples) # (123, 456)

num = 789
print(num, numTuples) # 789 (123, 456)
```

+ 四种数字类型：`int`、`long`(v3中不存在)、`float`、`complex`
```python
num_int = 123 # 整型
# num_long = 123L 长整型（v3中自动转化为int型）
num_float = 123.32 # 浮点型
num_complex = 123 + 3j # 复数型
```

+ 字符串、列表、元组截取
```python
"""
标识位不变，可以正负数混用：
H  e  l  l  o     W  o  r  l  d  !
0  1  2  3  4  5  6  7  8  9  10 11
-12-11-10-9-8 -7 -6 -5 -4 -3 -2 -1
"""

text = 'Hello World!'
print(text[1:3])  # el 永远为左包含关系[)
print(text[0:])  # Hello World! 从开头到结尾全部字符
print(text[-1:])  # ! 结尾字符开始到全部，只有个!
print(text[8:-2])  # rl 可以正负数混用，只要左右关系正确就行
print(text[1:9:2])  # el o 第三个数可选，为步长，默认为1，从截取范围隔两步取一位
print(text * 3)  # Hello World!Hello World!Hello World! *号表示重复次数
# 列表、元组截取道理相同
```

### 杂项

+ 语句结尾不推荐加分号

+ 用`"""`包裹多行文本，可以保持原有段落格式；非赋值时表示注释。例：
```python
# 段落赋值
text = """
    python:
Hello World!!!
"""

# 多行注释
"""
这是多行注释
"""
```

+ `print`默认打印结果换行，若想不换行，则用`,`分割

+ 变量必须初始化，否则出错

+ `python`不存在`++`、`--`运算符

+ `tuple`元组只有单个元素时，为保证结果准确必须添加`,`
```python
_tuple = ('all')
print(_tuple)  # all 不加','会被解析为单个字符串
real_tuple = ('all',)
print(real_tuple)  # ('all',)
```

+ 列表不可以作为字典的键值，因为它是可变的，字典键值要求是不可变的

## 版本差异（v2 & v3）

| name   | v2        | v3         |
|:-------|:----------|:-----------|
| 等待用户输入 | raw_input | input      |
| long类型 | 存在        | 不存在，用int代替 |
| 整数相除   | 结果为整数     | 结果可以为浮点数   |
