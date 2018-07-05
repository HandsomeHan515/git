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
