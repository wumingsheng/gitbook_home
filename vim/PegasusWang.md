# PegasusWang

- c-h删除上一个字符
- c-w删除上一个单词
- c-u删除到行首


- gi回到上一次编辑的地方

- w/W下一个单词开头
- e/E本单词的结尾
- b/B单词开头
- 大写和小写的区别是大写用空格作为单词的分隔符


- H文件开头M文件中间L文件结尾
- c-u/c-f翻页  zz光标在中间
- easy-motion插件

- daw/diw 删除单词   around包括空格inner不包括空格
- df/dt fchar/till
- w单词s句子p段落e文本整体


- 删除d/x
- 修改c/r/s    change replace substitute
- r替换一个字符R替换整行不断往后替换
- s删除一个字符进去插入模式S删除当前行进去插入模式

- * 和 # 高亮搜索当前单词    #和*的功能是一样的


- 替换 :[range]s[ubtitute]/{pattern}/{string}/[flags]
- range表示范围， 比如10,20表示10-20行   %表示全部行
- pattern表示要替换字符串的模式  string是替换后的文本
- flags标志
- g(global): 表示全局范围内执行
- c(confirm)：表示确认，可以确认或者拒绝修改
- n（number）: 不替换，显示匹配的数量 :%s/search//n



- 窗口之间的切换
- c-w-s水平分割 c-w-v垂直分割  或者:sp :vs 在nerdtree中使用i/s
- c-w-w循环切换
- c-w-{h、j、k、l}/{上下左右方向键} 按照方向切换 c-w是窗口切换的前缀
    大写的HKJL是窗口的切换不是光标的左右移动

- 文本对象
- [number]<command>[text-object]
- number次数
- command y（yank复制）d(delete删除) c(change修改)
- s句子 w单词 p段落 e(entity整个文本)
- i inner（不包括空格） a around（环绕包括空格）



- normal模式下粘贴系统剪切版的内容 `"+p`
- insert模式下粘贴系统剪切板的内容 `<c-r>+`
- 如果设置了autoindent的缩进问题，先:set paste   粘贴完成以后：set nopasts
- set clipboard=unnamed    系统剪贴版不用+寄存器，使用了无名寄存器这样y/p可以和系统交互















