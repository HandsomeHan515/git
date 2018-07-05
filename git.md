# Git 安装及使用

## 安装
  
地址：http://git-scm.com/download/
选择安装Git的环境 Windows、Mac、Linux 下载对应版本
下载完成，点击exe一路安装即可
输入命令行：git --version
输出git版本号表示git安装成功 如：git version 2.6.4

## 配置本机用户信息

+ git config --global user.name "你的用户名"
+ git config --global user.email "你的邮箱"

## 项目地址

+ HTTPS：读写仓库加密通道，有单次上传限制。
+ SSH：读写仓库加密通道，无单次上传限制，需先在个人设置页面上传 SSH-RSA 公钥，完成配对验证。

## SSH公钥配置

```code
ssh-keygen -t rsa -C "你的邮箱" // 按回车，生成id_rsa.pub文件
ls ~/.ssh // 根目录查看是否有 id_rsa.pub 文件
cat ~/.ssh/id_rsa.pub // 查看 id_rsa.pub 文件
// 复制id_rsa.pub文件中所有内容，粘贴到公钥内容
```

## git本地仓库

要对现有的某个文件夹开始用Git管理，需切到所在的目录，执行：
git init   把当前目录变成git可以管理的仓库
该目录下会有一个.git的目录，这个目录是Git用来跟踪管理版本的

也可以直接通过 git clone 命令来直接复制远程仓库到本地目录
git clone git@git.coding.net:xiaocuo/test.git mywork
上述命令将在当前位置新建一个名为“mywork”的文件夹，内容为远程test项目中的文件

## 代码 提交

```code
git add .  (点表示当前目录下所有文件添加到暂存区，也可指定具体文件)
git commit -m '提交日志'  把暂存区的所有内容提交到当前分支上
git remote add origin git@git.coding.net:xiaocuo/page.git  添加远程仓库
git push -u origin master   将改动提交到远程仓库
git pull git@github.com:xiaocuo/page.git 将远程仓库的改动更新到本地

git status  查看代码的当前状态
git log   显示提交纪录
git branch  显示所有分支列表，创建分支,比如：git branch bigChange
git checkout bigChange   切换到之前创建的分支
```