# Numpy

## 简介
Numpy是Python的一种开源数值计算扩展库。

Numpy包的核心是ndarray对象，即n维数组，本质上是对Python列表类型的扩展，包含了很多对数组的运算和操作函数，如求和、平均值、方差等。

官方文档：https://www.numpy.org.cn/

## 优势
Numpy具有如下优点：
1. 运算速度快
2. 扩展性强
3. 使用简单

## 使用
因Numpy是对数组进行运算，因此在使用时首先要得到一个ndarray对象。

### 导包
```python
import numpy as np
```

#### 生成

#### 一维数组
```python
# 将列表转换为ndarray对象
np.array(list)

# 生成从from到to，间隔为gap的数组
np.arrange(from, to, gap)
```

#### 矩阵
```python

# 全0
np.zeros(shape=(3,5), dtype=np.float16)

# 全1
np.ones(shape=(3,5,2), dtype=np.int8)

# 任意填充值
np.full(shape=(3,5), fill_value=5.2)


```

