:material-information-outline:{ title="Important information" } 前置条件: `Github账户`、`梯子(选)`

:material-information-outline:{ title="Important information" } 软件环境：`python 3.8+`、`git bash`、`文本编辑器`

## 1. 必要软件环境的安装

### Git Bash
首先需要安装 `git bash`，直接点 [这里](https://github.com/git-for-windows/git/releases/download/v2.45.2.windows.1/PortableGit-2.45.2-64-bit.7z.exe) 下载并运行，一路点确定就可以了喵

验证安装：在终端 **cmd**(1) 或 **Powershell**(2) 中输入 `git -v` 命令，返回版本信息即成功
{ .annotate }

1.  打开方式：`Win + R`，输入 `cmd` 回车打开

2.  打开方式：`Win + R`，输入 `powershell` 回车打开

![](http://imgs.alphasword.xyz/TUCIM-GUIDE/git-v.png)

### 文本编辑器
为了能够方便地编辑多文件文档，我们推荐使用 **VSCode** 编辑器 (建议使用微软商城 Microsoft Store 安装，鬼知道百度出来的那一堆是什么牛马东西)

就像我现在这样
![](http://imgs.alphasword.xyz/TUCIM-GUIDE/vsc.png)

### Mkdocs-Material依赖

在终端界面输入如下命令安装依赖包

```shell
pip install mkdocs-material
```

若下载过慢可参考 [常见问题](troubleshooting.md) 的 `#1` ，对pip换源

## 2. 克隆项目 & 提交修改
1.首先打开到本项目的 [仓库页面](https://github.com/teriyakisushi/tucim)，点击右上角的 `Fork` 按钮，将本项目克隆到你的Github账户下

![](http://imgs.alphasword.xyz/TUCIM-GUIDE/fork.png)

2.此时你的仓库列表（Your Repositories）中会出现 `tucim` 的项目，点击进入，复制项目地址

![](http://imgs.alphasword.xyz/TUCIM-GUIDE/repo_new.png)


3.在本地任意位置新建目录，在该目录下按 <kbd>Shift</kbd> + <kbd>鼠标右键</kbd> 选择 `使用终端打开`，输入如下命令

```shell
git clone <你的项目地址>
```

4.如果你是首次使用git bash，会提示你输入Github账户密码，按要求输入即可
</br>接下来等待clone操作完成

![](http://imgs.alphasword.xyz/TUCIM-GUIDE/clone.png)

5.完成后，你的目录下会出现一个 `tucim` 文件夹，这就是我们的项目文件夹
</br>接下来我们得在本地新建一个分支，输入如下命令

```shell
git checkout -b <你的分支名>
```

6.现在可以开始编辑文档了，编辑请参照[编辑规范](main.md)，完成后，我们需要将修改提交到远程仓库上，输入如下命令

```shell
git add .
git commit -m "你的提交信息"
git push origin <你的分支名>
```

![](http://imgs.alphasword.xyz/TUCIM-GUIDE/pushtips.png)

7.完成后，你可以在你的Github仓库中看到你的修改，点击 `Pull Request` 按钮，提交你的修改到本项目仓库，等待我们审核即可，至此你已经完成了编辑贡献！

## 3.与本项目同步
当本项目有更新时，你需要将本项目的更新同步到你的项目中，输入如下命令

```shell
git remote add upstream https://github.com/teriyakisushi/tucim #(1)
git fetch upstream #(2)
git merge upstream/main #(3)
```

1.  添加上游仓库为远程仓库
2.  获取上游仓库的更新
3.  合并更新到你的本地分支

