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
因Numpy是对数组进行运算，因此在使用时首先要得到一个ndarray对象（多维数组）。

### 导包
```python
import numpy as np
```

### 生成ndarray

#### 一维数组
```python
# 将列表转换为ndarray对象
np.array(list)

# 生成从from到to，间隔为gap的数组
np.arrange(from, to, gap)

# 等差数列（左闭右闭）
np.linspace(0, 100, num = 101)
```

#### 矩阵
```python

# 全0
np.zeros(shape = (3, 5), dtype = np.float16)

# 全1
np.ones(shape = (3, 5, 2), dtype = np.int8)

# 任意填充值
np.full(shape = (3 ,5), fill_value = 5.2)

# 对角线为1的数列
np.eye(N = 5)

# 随机生成
np.random.randint(0, 100, size = (5, 5))

# 生成0-1的随机数（左闭右开）
np.random.random(size = (2, 3))

# 标准正态分布（平均值0，方差1）
np.random.rand(4, 5)

# 正态分布
np.random.normal(loc = 0.0, scale = 1.0, size = None)

```

### ndarray常用属性
size: 个数

shape: 形状

ndim: 维度

dtype: 类型

### 计算
```python
# 求和
nd.sum()

# 均值
nd.mean()

# 方差
nd.var()

# 标准差
nd.std()
```

### 切片（规则和python列表一致）
```python
# 前三行，前三列
nd[0:3, 0:3]

# 反转（本质是间隔取数）
nd[::-1]
```

#### 利用切片修改图片
图片本质上是三维数组（高度，宽度，色值）
```python
# 引入图片库
from PIL import Image

# 打开图片
pic = Image.open('xx.jpg')

# 转换为ndarray
pic_nd = np.array(pic)

# 利用切片操作图片
# 变绿（本质是切换颜色索引）
Image.fromArray(pic_nd[:, :, [1, 0, 2])
# 尺寸压缩（隔5取1）
Image.fromArray(pic_nd[::5, ::5])
# 去色（去除最后一维）
Image.fromArray(pic_nd[:, :, 0])

# 引入图片操作库
import matplotlib.pyplot as plt
%matplotlib inline

# 显示图片
plt.imshow(pic_nd)
```

### 操作
```python
# 变形
np.reshape(3,4)

# 转置（axe为转置索引）
np.transpose(pic_nd, axes = (1, 0, 2))

# 级联（数组合并，1行4列*2 = 2行4列）
np.concatenate([pic_nd, pic_nd])

# 按指定方向级联（axis参数为级联维度下标，如二维行列数组，列下标为1）
# 按列级联
np.concatenate([nd1, nd2], axis = 1)
```
