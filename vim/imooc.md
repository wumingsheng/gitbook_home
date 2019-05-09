# imooc:

## 1. 文本对象

- {operator}{a}{object}
- {operator}{i}{object}


说明：

+ a: 包含收尾
+ i: 只是内容本身，不包含收尾

### 1.1 object

| textobj                        |     说明                |
| ----------                     |  -------                |
| w                              |     word                |
| s                              |     sentence            |
| p                              |     paragraph           |
| e                              |     entire              |
| 重复执行两次                   |     当前行              |
| []、()、{}、""、`<tag>`        |     括号和标签[t]       |



> e对象，整个文本，需要借助插件【vim-textobj-user】【textobj-entire】


### 1.2 operator

- `v` : 可视选中
- `y` : 复制
- `p` : 粘贴
- `c` : 修改
- `d` : 删除
- `x` : 剪贴
- `>` : 缩进
- `g~`: 大小写转换【gu、gU】

> 如果重复执行，代表作用当前行







