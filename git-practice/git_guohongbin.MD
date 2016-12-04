# Git 笔记

## 版本控制管理
1. 本地版本控制
2. 集中化的版本控制 CVSC，如 SVN
3. 分布式版本控制 DVCS，如 Git

## Git 的基础了解
* 三种状态： Committed（Git 仓库）、Modified（工作目录）、Staged（暂存区域）

## Git 的安装与配置
### 安装
在 Mac 理直接安装 Xcode Command Line Tool 并运行git 即可。
### 配置

#### git config 
用以配置 git 外观和行为，存储在:
* /etc/gitconfig 通用的配置 （--system）
* ~/.gitconfig ~/.config/git/config 当前用户配置 （--global）
* .git/config 对当前仓库

#### 用户信息
* git config --global user.name "Ia someone"
* git config --global user.email "Ia@some.com"

#### 查看
* git config <key>
* git config --list
* git help <verb>
* git <verb> --help
* man git-<verb>

## Git 的使用
### 基础使用
#### 初始化
`git init`
#### 添加 
Git 可以用 git http https ssh 等协议
`git add *.*`

`git add LICENSE`

`git commit -m 'initial project version'`

`git clone [url] [name]`

#### 查看
`git status`

`git log`

`git log -p -number`

`git log --stat`

#### 忽略
.gitignore，支持简化正则表达式

#### 比较
`git diff <--staged/cached>`

#### 提交
`git commit`
跳过使用暂存区域
`git commit -a -m`

`git commit --amend`
#### 删除
`rm somefile`

`git rm somefile`
#### 移动
`git mv file_from file_to`

#### 撤销
checkout 一下

`git checkout --somefile`

### 远程
#### 远程添加
`git remote -v`


`git remote add <shortname> <url>`

#### 抓取与拉取
* 抓取
`git fetch [remote-name]`
* 拉取
`git push origin master`
#### 查看
`git remote show origin`

#### 重命名
`git remote rename pb pual`

#### 删除
`git remote rm paul`

### 标签
* `git tag <-l> 'someword'`
* `git tag -a <sometag>`
* `git log --pretty=oneline` `git tag -a v1.2 something`
* `git push origin v1.5`
* `git checkout -b [branchname]`

## branch
### 创建与切换
* `git branch testing`
* `git log --oneline --decorate`
* `git checkout testing`
* `git commit -a -m 'made a change`

### 合并
* `git merge hotfix`

### 分支的管理
#### 分类 
长期分支、特性分支 、远程分支

#### 变基
`git rebase master`
