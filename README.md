# Git 简介

> Git是目前世界上最先进的分布式版本控制系统（没有之一）。

## 创建版本库

```code
mkdir git
cd git
git init
git add README.md
git add git.md
git commit -m 'first commit'
```

## 版本回退

```code
git log // 查看提交历史
git reflog // 查看操作历史
git reset --hard commit_id
```

## 工作区和暂存区

+ 第一步是用 git add 把文件添加进去，实际上就是把文件修改添加到暂存区；
+ 第二步是用 git commit 提交更改，实际上就是把暂存区的所有内容提交到当前分支。
+ 使用 git status 查看状态

## 撤销修改

+ 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令 git checkout -- file。
+ 场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令 git reset HEAD < file >，就回到了场景1，第二步按场景1操作。
+ 场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

## 删除文件

```code
git rm git.txt
git commit -m 'delete git.txt'
git push
```

## 创建与合并分支

+ 查看分支：git branch
+ 创建分支：git branch < name >
+ 切换分支：git checkout < name >
+ 创建+切换分支：git checkout -b < name >
+ 合并某分支到当前分支：git merge < name >
+ 删除分支：git branch -d < name >