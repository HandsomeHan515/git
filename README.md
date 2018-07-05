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