# 命令行工具

## 1. zsh

```
sudo apt-get install git -y
sudo apt install zsh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

```

## 2. ag：比grep、ack更快的递归搜索文件内容

```bash
sudo apt-get install silversearcher-ag

Usage: ag [FILE-TYPE] [OPTIONS] PATTERN [PATH]

  Recursively search for PATTERN in PATH.
  Like grep or ack, but faster.

Example:
  ag -i foo /bar/
```
使用

```bash

$ ag -i apt-get .

```







## 3. tig：字符模式下交互查看git项目，可以替代git命令



```bash
sudo apt-get install tig
```





## 4. ## mycli


```bash
sudo apt-get install python-pip
sudo pip install mycli
mycli -u root
```

## 5. jq: json文件处理以及格式化显示，支持高亮，可以替换python -m json.tool。

```bash
sudo apt-get install jq

jq - commandline JSON processor [version 1.5-1-a5b5cbe]
Usage: jq [options] <jq filter> [file...]


```

使用

```bash
$ curl localhost:8080/aaa|jq .map.age   
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   107    0   107    0     0  26750      0 --:--:-- --:--:-- --:--:-- 26750
13

```


如果是数组的话，需要加引号

```bash
$ curl localhost:8080 -s|jq '.data[0].addr[1]'

```


选项：

* -c : 单行输出
* -R : 原生输出



## 6. fzf：命令行下模糊搜索工具，能够交互式智能搜索并选取文件或者内容，配合终端ctrl-r历史命令搜索简直完美


```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```


- CTRL-T：搜索文件和目录
- CTRL-R：搜索历史命令
- ALT-C：列出当前文件夹下的目录




## 7. curl

```bash
curl localhost:8080/user/save -X POST -H "Content-Type: application/json" --data '{"id":"2","username":"jack","password":"123","status":"ENABLED"}'
```




## 8. neovim

## 9. tmux


```bash
sudo apt-get install tmux
```

ctrl+b => tmux prefix

**layouts 布局**

1. server 服务
2. session 回话
3. window 窗口
4. pane 窗格

**window 窗口**

- c - new a window   新建窗口
- & - close current window 关闭窗口
- l - switch to last window 切换窗口

- n - next window   切换到下一个窗口
- p - previous window 切换到上一个窗口

- w - show window ment list 窗口的菜单列表

**pane 窗格**

- % - horizontal split 垂直分屏
- " - vertical split 水平分屏

- x - close current pane 关闭窗格
- ; - switch to last pane 切换窗格
- o - swtich pane clockwise 顺时针转换窗格
- C-o - swap pane anti-clockwise 逆时针转换窗格

## 10 autojump

```bash
sudo apt install autojump -y
source /usr/share/autojump/autojump.sh
```


```zshrc
plugins=(git autojump)


source /usr/share/autojump/autojump.sh

source $ZSH/oh-my-zsh.sh
```
source .zshrc


使用

j 目录
要跳到目录，首先需要cd 到目录一次






