# 02 仓库 Repository

仓库，英文叫 Repository，简称 repo。

大白话说：一个 Git 仓库就是一个被 Git 管起来的项目文件夹。

只要一个文件夹里面有 `.git` 目录，它就是 Git 仓库。

## 本地仓库

本地仓库就是你电脑上的项目。

```text
D:\TongTianLu\Lesson\git-learn
```

这个目录已经执行过：

```powershell
git init
```

所以它现在就是一个 Git 仓库。

## 远程仓库

远程仓库就是放在服务器上的仓库，比如 GitHub 上的：

```text
https://github.com/hencter/git-learn
```

## 本地和远程的关系

```mermaid
flowchart LR
  Local["本地仓库<br/>你的电脑"]
  Remote["远程仓库<br/>GitHub"]

  Local -- "git push 上传" --> Remote
  Remote -- "git pull 拉取" --> Local
```

## 常用命令

```powershell
# 初始化当前文件夹为 Git 仓库
git init

# 查看当前远程仓库地址
git remote -v

# 查看当前仓库状态
git status
```

## 相关概念

- [[01 Git 是什么]]
- [[05 远程仓库 Remote]]
- [[06 GitHub 和 GitHub CLI]]
