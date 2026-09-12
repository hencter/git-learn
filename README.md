# GitHub CLI 简单说明

GitHub CLI，也叫 `gh`，就是 GitHub 官方出的命令行工具。

平时我们操作 GitHub，经常要打开浏览器，比如创建仓库、看 issue、创建 PR。装了 `gh` 以后，很多事情可以直接在终端里完成。

## 仓库索引

- [GitHub 本周趋势报告：2026-09-12](reports/github-trending-2026-09-12.md)
- [Obsidian Git 知识图谱](obsidian/git-knowledge-graph/Git%20%E7%9F%A5%E8%AF%86%E5%9B%BE%E8%B0%B1.md)

## 看看有没有安装成功

```powershell
gh --version
```

如果能看到版本号，就说明安装好了。

## 登录 GitHub

```powershell
gh auth login
```

它会一步一步问你怎么登录。一般按默认选项就可以：

- 选择 `GitHub.com`
- Git 操作方式选择 `HTTPS`
- 登录方式选择 `Login with a web browser`

然后它会给你一个验证码，并打开 GitHub 网页。把验证码填进去，授权完成后，电脑上的 `gh` 就登录好了。

## 看自己有没有登录

```powershell
gh auth status
```

如果看到 `Logged in`，就说明已经登录成功。

## 常用命令

```powershell
# 查看当前登录状态
gh auth status

# 在 GitHub 上创建一个仓库
gh repo create

# 把 GitHub 上的仓库克隆到本地
gh repo clone 用户名/仓库名

# 查看当前仓库的 pull request
gh pr list

# 创建一个 pull request
gh pr create

# 查看 issue
gh issue list

# 用浏览器打开当前 GitHub 仓库页面
gh browse
```

## 把本地项目上传到 GitHub

如果你已经在本地写好了项目，可以这样做：

```powershell
git status
git add .
git commit -m "第一次提交"
gh repo create --source . --remote origin --push
```

这几行的意思是：

- `git status`：看看哪些文件改了
- `git add .`：把当前目录下的改动都加入 Git
- `git commit -m "第一次提交"`：保存一次提交记录
- `gh repo create --source . --remote origin --push`：在 GitHub 上创建仓库，并把当前代码推上去

## 不知道命令怎么用怎么办

可以用帮助命令：

```powershell
gh help
gh repo --help
gh pr --help
```

简单理解：`gh` 负责帮你操作 GitHub，`git` 负责管理你本地的代码版本。两个工具经常一起用。
