# Git入门学习笔记

## 参考资料

【git官方教程（文档、书籍、视频）】[https://git-scm.com/doc](https://git-scm.com/doc) 

【Git五分钟教程】[https://www.runoob.com/w3cnote/git-five-minutes-tutorial.html](https://www.runoob.com/w3cnote/git-five-minutes-tutorial.html) 

【B站视频教程】 [https://www.bilibili.com/video/av8261658/?p=10](https://www.bilibili.com/video/av8261658/?p=10) 

【文字教程-廖雪峰】 [https://www.liaoxuefeng.com/wiki/896043488029600](https://www.liaoxuefeng.com/wiki/896043488029600) 

【文字教程-菜鸟驿站】[https://www.runoob.com/git/git-tutorial.html](https://www.runoob.com/git/git-tutorial.html) 

【linux系统下从安装到使用流程】[https://www.cnblogs.com/huiyichanmian/p/9820024.html](https://www.cnblogs.com/huiyichanmian/p/9820024.html) 

【cheat sheet】[https://gitee.com/liaoxuefeng/learn-java/raw/master/teach/git-cheatsheet.pdf](https://gitee.com/liaoxuefeng/learn-java/raw/master/teach/git-cheatsheet.pdf) 

【cheat sheet 02】[https://www.cnblogs.com/franzz/p/9864188.html](https://www.cnblogs.com/franzz/p/9864188.html) 

【git community book 中文版】[http://gitbook.liuhui998.com/index.html](http://gitbook.liuhui998.com/index.html) 

【互联网组织的未来：剖析GitHub员工的任性之源[https://www.runoob.com/w3cnote/internet-organization-github.html](https://www.runoob.com/w3cnote/internet-organization-github.html)

## 清单

### git基本操作

```bash
git init	　　　　##创建git仓库
git add	xxx 　　##将本地文件xxx的修改提交到暂存区
git commit -m "mx"	##将暂存区的所有修改修改提交到仓库当中
git reset --hard HEAR^	##本地目录恢复到上一个版本
git reset --hard xxx	##恢复本地目录至版本xxx
git log	##查看提交日记
git status	##显示工作目录和暂存区的状态
git diff	##比较当前文件和暂存区文件的差异
git diff HEAR HEAR^
```

### 远程仓库

#### 查看

```bash
git remote	#查看远程仓库(简单描述)
git remote -v	#查看远程仓库(详尽描述)
```

#### 添加和移除

```bash
git remote add origin git@github.com:Franzzt/xxx.git	##添加名为origin的远程仓库
git remote rm origin
```

#### clone

```bash
git clone 仓库地址
#checkou远程分支feature,在本地起名为feature,并切换到分支feature
git checkout -b feature origin/feature 

仓库中获取源码分为两种方式：
1.获取所有的项目源码，
git clone git@github.com:Franzzt/learngit.git 下载整个项目的源码

2.获取单个分支的源码
git clone -b origin/dev git@github.com:Franzzt/learngit.git 只下载分支dev的源码

不同的是下载整个项目的源码之后可以在整个项目的所有分支中来回切换，
而下载单个分支的动作之后则无法切换到其他分支
```

#### push

```bash
git push <远程主机名> <本地分支名>:<远程分支名>
git push -u origin master	##推送主分支master到仓库origin
git push -u origin feature-A	##推送分支feature-A到仓库feature-A
git push 推送当前分支到仓库
```

#### pull/fetch/merge

```bash
git pull <远程主机名> <远程分支名>:<本地分支名>	##取回远程库更新，并与本地分支合并
git pull origin feature

git fetch	##将远程的所有分支跟新到本地
git fetch <远程主机名> <分支名>	##取回远程特定分支的更新
git fetch origin
git merge origin/next
```

### 分支

```bash
git branch	##查看本地分支
git branch -r ##查看远程分支
git branch -a	##查看所有分支

git branch feature	##以当前所在分支创建新分支feature
git checkout feature	##切换到分支feature
git checkout -b feature	##创建分支feature并切换到分支feature

git merge feature	##将分支feature内容合并到当前所在分支

git branch -d feature	##删除本地分支feature
git push origin --delete feature	##删除远程仓库分支feature

git push origin dev	##推送分支dev至远程仓库
git branch --set-upstream-to=origin/dev dev # 建立本地分支和远程分支的关联
```

```text
master分支    是主分支，要时刻与远程同步，一般我们发布最新版本就用master分支。
develop分支    是开发分支，团队中所有人都在这个分支上开发，所以也需要与远程同步。
bug分支    一般只在本地使用来修复bug，一般不需推送远程仓库中。
feature分支    是否需要推送到远程，要看是不是有几个人合作开发新功能，如果你是一个开发，那就留在本地吧。
release分支    一般是系统管理，推送或抓取的分支一般与开发人员无关。
other分支    按需求分配。
```

### 多人协作

```bash
github上创建仓库(仓库地址：git@giithub.com:Franzzt/xxx.git)
git init
git remote add origin git@giithub.com:Franzzt/xxx.git
git remote(查看)
git add tset.txt
git commit -m "first file"
git push -u origin master
git checkout -b devlop
git add text.txt
git commit -m "add text.txt file to branch devlop"
git push -u origin devlop
git checkout master
git merge devlop
git fetch origin master
git diff
git add
git commit -m
git push origin master
git pull origin master
git git branch --set-upstream-to=origin/devlop
modify file
#or
#18.git fetch origin master
#19.git diff
#20.git merge
```

## 我的尝试

```bash
git config user.name 'KiwiAp'
git config user.email '347943085@qq.com'
git config -l

mkdir testgit
cd testgit
git init
echo "# testgit" >> README.md
git add README.md
git commit -m "test first commit"

echo 'A change' >> README.md
git status
git add .
git commit -m 'test a change'
git log
git log --online
git reflog

echo 'test reset' >>README.md
git add .
git status
git reset HEAD
git diff
git status
git checkout

git remote add origin https://github.com/KiwiAp/ttestgit.git	#叫origin的远程仓库
git push -u origin master
git pull
```

