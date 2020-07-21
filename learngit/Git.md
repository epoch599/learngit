# 安装Git

按照默认设置安装，安装好设置用户名及邮箱。

```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```



# 创建版本库

首先创建一个空目录。

```
$ mkdir learngit
```

然后通过`git init`命令把这个目录变成Git可以管理的仓库。

```
$ git init
```

## 把文本添加到文本库

首先用命令`git add`把文件添加到暂存区。

```
$ git add readme.txt
```

然后用命令`git commit`把文件提交到当前分支。

```
$ git commit -m "wrote a readme file"
```



# 文本操作

通过`git status`命令查看此时文本状态。

```
$ git status
```

通过`git diff`命令查看文本修改内容。

```
$ git diff readme.txt 
```

通过`git log`命令查看最近到最远的提交日志。

```
$ git log
```

```
$ git log --pretty=oneline
```

通过`git reset`命令回退到上一版本。

```
$ git reset --hard HEAD^
```

通过`cat`命令查看文本内容。

```
$ cat readme.txt
```

通过`git reflog`查看每一次命令。

```
$ git reflog
```

通过`git checkout -- file`丢弃工作区的修改。

```
$ git checkout -- readme.txt
```

通过`git reset HEAD <file>`把暂存区的修改撤销掉，重新放回工作区。

```
$ git reset HEAD readme.txt
```

通过`git rm`删除版本库中的文件。

```
$ git rm test.txt
```

通过以下命令将远程仓库与本地仓库进行关联。

```
$ git remote add origin git@github.com:epoch599/learngit.git
```

通过以下命令将本地库的内容推送到远程库。

```
$ git push -u origin master
```

通过以下命令将远程库的内容拷贝到本地库。

```
$ git clone git@github.com:epoch599/gitskills.git
```