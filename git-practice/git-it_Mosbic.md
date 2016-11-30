# GIT-IT 教程笔记
[TOC]
nodeschool教程见[这里](http://nodeschool.io/zh-cn/).
git 版本控制
在终端输入
`npm install -g git-it`后输入
`git-it`运行
通过说明可以找到一个繁体中文网址，[Git-it](http://jlord.us/git-it/index-zhtw.html).
## 安装并且设定Git
 显示版本
 `git --version`

设定名字和邮箱
 `git config --global user.name "<Your Name>"`
 `git config --global user.email "<youremail@example.com>"`

## 建立本机的repository仓库
repository在上文的翻译中称作 程式库，即程序仓库。
建立新的文件夹 `mkdir <文件夹名>`
进入这个文件夹`cd <文件夹名>`
列出文件夹内容 mac`ls` windows    `dir`
把这个文件夹设定成一个git文件夹 `git init`  init 表示的是initial，不是在里面
输入`git status`来查看状态

## 检查状态，新增或修改commits
查看状态`git status`
建立新文件后并**准备**提交修改
`git add <新文件>`
**准备**提交对所有文件的修改
`git add .`
提交准备好的修改并提交简短信息为变动说明
`git commit -m <commit信息>`
查看那些有存在差异的文件，查看问文件的修改
`git diff`


## 注册Github账户
注册好要告诉Git你的Github帐号是什么[^说明]
`git config --global user.username <UserName> `

## 将repository仓库做本机和远端的连结
在 remote（GitHub 上）新建了一个repository。在repository 的頁面上你會看到一個 'Quick Setup' 的部份，確認選擇的網址是 'HTTP'，而不是 'SSH'，右邊的欄位就是這個 遠端的remote 程式庫repository 在 GitHub 主機上的位址。

回到終端機，在我們剛剛初始化過 Git 的 'hello-world' 的資料夾裡頭，我們需要告訴 Git 這個 遠端remote 的位址。同一個 Git 專案中，可以有很多不同的 遠端remote，所以每一個 遠端remote 都需要一個名字。而最主要、原始的那一個，通常都是叫做 origin。

新增remote连结
` git remote add origin <URLFROMGITHUB>`
你電腦上的 程式庫repository 現在知道了專案有一個在 GitHub 上的 遠端remote，叫做 'origin'。你可以想像這就好像是把一個電話號碼配上一個名字一樣，這樣當你要打電話的時候，就不用記得號碼了。

### 收取远端
`git pull <REMOTENAME> <BRANCHNAME>`
## 查看有哪些远端连结
`git remote -v`
### 推送到远端
本地最初的分支通常叫 master， 想要把本地的branch *master* 推送到远端的*origin*
`git push origin master`


## 复制fork和克隆clone一个开源计划
在github上建立fork复本（可以自己修改的仓库），并下载clone到本地
`git clone <URLFROMGITHUB>`
收取最原始的程序库，通常用upstream来表示这个原始的远端
`git remote add upstream <URL>`
## 建立一个feature分支branch

![](./_image/2016-09-15 21-40-18.jpg)
`git  status`
新增分支
`git branch <BRANCHNAME>`
取出checkout新增的分支
`git checkout <BRANCHNAME>`

常用
```git
git status //看目前在哪个分支
git branch //列出分支
git checkout -b <BRANCHNAME>//新增并切换到新分支
git branch -M <NEWBRANCHNAME> //修改branch名字 重命名当前分支
git status
git add <FILENAME>
git add -A // 会讲新增档案和删除档案的动作一起记录下来
git commit -m '<COMMIT MESSAGE>'
// 之后将修改好的仓库推送push到github上
git push origin <BRANCHNAME>


```


## 利用push和pull来和Github同步
在收取更新之前检查远端是否有变动
`git fetch --dry-run`
从远端remote收取pull更新
`git pull <REMOTENAME> <BRANCH>`
某些情况下可以直接`git pull`
复制repo到本地电脑
`git clone <URL>`
新增remote的连结
`git remote add <remotename> <URL>`
检查现有的远端连结
`git remote -v`


##建立一个pull request 
到原来的仓库发送一个收取请求pull request
参考[这里](http://jlord.us/git-it/challenges-zhtw/requesting_you_pull_please.html)
我的经验是在自己复制的复本里进行pull request
## 合并merge和删除delete 分支branch
把复本和原始的repo同步，把本地的分支合并进主要分支
切换大想要合并进去的分支
`git checkout <主分支>`
之后合并到目前分支
`git merge <要合并的功能分支名称>`
然后可以删除本机已经合并过的功能分支
`git branch -d <之前的分支>`
你的forked repo中删除旧分支
`git push <REMOTENAME> --delete <BRANCHNAME>`

从上游远端分支名称通常叫upstream收取
`git pull <远端分支名称> <BRANCHNAME>`
[^说明]:  对于同时使用Github和其他如Gitlab的方式，建议使用SSH做相应的修改。