

# 进阶用法


### expression for item in iterable

**遍历可迭代对象中的每个元素并直接保留原值‌**

```
示例：

# 传统循环写法
result = []
for p in numbers:
    result.append(p)  # 等价于 [p for p in numbers]

numbers = [1, 2, 3, 4]
result = [p for p in numbers]
print(result)  # 输出: [1, 2, 3, 4]

# 保留偶数
even_numbers = [p for p in numbers if p % 2 == 0]

```

### for i, data in enumerate(testLoader, 0)

**用于在遍历序列（如列表、元组、字符串）时同时获取索引和元素值**

```
for i, item in enumerate(['a', 'b', 'c'], start=1):
    print(i, item)  # 输出 1 a, 2 b, 3 c
```


### for p1, p2 in zip(data1, data2)

**同时遍历多个序列，每次取出相同位置的元素组合成元组，以最短的输入序列长度为标准**

```
示例：
data1 = [1, 2, 3]
data2 = ['a', 'b', 'c']

for p1, p2 in zip(data1, data2):
    print(p1, p2)
输出：1 a  2 b  3 c

#‌解压为列表
list(zip(data1, data2))  # 输出 [(1,'a'), (2,'b'), (3,'c')]

#‌不等长序列处理
from itertools import zip_longest
list(zip_longest(data1, data2, fillvalue='X'))

#矩阵转置
matrix = [[1,2], [3,4], [5,6]]
list(zip(*matrix))  # 输出 [(1,3,5), (2,4,6)]
```

## 文件操作
