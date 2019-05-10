# vim实用技巧

![](/assets/20190509131045.png)

## 查看缓冲区文件、切换缓冲区文件

`:ls` 查看缓冲区文件   也可以使用`:files` or `:buffers`

> 还可以使用:Buffers     改命令来自于插件

- `:buffer` n 切换缓冲区文件   可以简写成:b 5
- `:bnext`下一个缓冲区文件 , 简写bn
- `:blast` 上一个缓冲区文件， 简写bl
- `:jumps`
- 使用快捷键`<c-o>/<c-i>`


## 2. 使用符号或标签包裹单词

借助插件`https://github.com/tpope/vim-surround`

1. 可视模式下，选中单词 
2. S": 添加
3. cs"'：修改双引号变成单引号（修改的话只需要放在inside,不用可视化选中）







