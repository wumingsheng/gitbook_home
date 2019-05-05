# 命令行工具

## 1. zsh

```
sudo apt-get install git -y
sudo apt install zsh
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

```

## 2. ag：比grep、ack更快的递归搜索文件内容

```
sudo apt-get install silversearcher-ag
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
```


## 6. fzf：命令行下模糊搜索工具，能够交互式智能搜索并选取文件或者内容，配合终端ctrl-r历史命令搜索简直完美


## 7. curl

```bash
curl localhost:8080/user/save -X POST -H "Content-Type: application/json" --data '{"id":"2","username":"jack","password":"123","status":"ENABLED"}'
```





