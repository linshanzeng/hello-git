# Git简介

## 安装Git

查看系统有没有安装Git：git

指定用户名和邮箱：

```text
git config --global user.name "chiyisan"
git config --global user.email "chiyisan@gmail.com"
```

## 创建版本库

初始化一个Git仓库：git init

把文件添加到仓库：

```text
git add readme.txt
git commit -m “wrote a readme file”
```

一次提交多个文件：

```text
touch file1.txt file2.txt file3.txt
git add file1.txt
git add file2.txt file3.txt
git commit -m "add 3 files."
```

# 时光机穿梭

查看工作区状态：git status

查看修改内容：git diff readme.txt

## 版本回退

查看提交历史：git log

查看简化提交历史：git log --pretty=oneline

回退到上一个版本：git reset --hard HEAD^

回退到指定版本：git reset --hard 52b34

查看命令历史：git reflog

## 管理修改

查看工作区和版本库里面最新版本的区别：git diff HEAD -- readme.txt

## 撤销修改

丢弃工作区的修改：

```text
方法一：
git restore readme.txt
方法二：
git checkout -- readme.txt
```

丢弃暂存区的修改：

```text
git add readme.txt

方法一：
git restore --staged readme.txt
方法二：
git reset HEAD readme.txt
```

## 删除文件

```text
git commit -m "add test.txt"
rm test.txt

删除文件：
git rm test.txt
git commit -m "remove test.txt"
还原删除文件方法一：
git restore test.txt
还原删除文件方法三：
git checkout -- test.txt
```

# 远程仓库

创建SSH Key：

```text
ssh-keygen -t rsa -C "chiyisan@gmail.com"
cat ~/.ssh/id_rsa.pub
```

## 添加远程仓库

关联一个远程库：git remote add origin git@github.com:linshanzeng/hello-git.git

首次推送到远程库：git push -u origin master

非首次推送到远程库：git push origin master

删除远程库：

```text
查看远程库信息：git remote -v
删除本地和远程的绑定管理：git remote rm origin
```

# 关联链接

[hello-git2](https://github.com/linshanzeng/hello-git2)

# 参考链接

[Git教程](https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496)
