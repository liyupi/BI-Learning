# Jupyter

## 简介
一款Python交互式笔记本，通过web访问，文件后缀为`.ipynb`。

## 使用
打开Anaconda目录下的Jupyter Notebook，访问web网址，可输入python代码。
具有Code和Markdown两种模式。

### 快捷键
内置多种快捷键，如`ctrl + enter`等。

通过`M`切换Jupyter为Markdown模式。

### 魔法指令

Jupyter自带的特殊指令，完成特殊功能，使其更加灵活。

查看所有魔法指令：
```python
%lsmagic
```

#### 运行时间

计算当前行
```python
%time sum(x)
```

计算多行
```python
%%time
sum1(x)
sum2(x)
```

计算多次运行平均时间
```python
%%timeit
```

#### 系统命令
魔法指令支持大多数Linux命令，如`%cd`、`%ls`、`%mkdir`等。
