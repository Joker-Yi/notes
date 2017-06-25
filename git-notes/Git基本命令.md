# Git 安装教程

#### Debian / Ubuntu 安装教程
安装命令为：
``` shell
# 安装扩展工具包
$ sudo apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \ libz-dev libssl-dev

# 安装 Git 核心工具包
$ sudo apt-get install git-core
```

#### CentOS / RedHat 安装教程
安装命令为：
``` shell
# 安装扩展工具包
$ sudo yum install curl-devel expat-devel gettext-devel \ openssl-devel zlib-devel

# 安装 Git 核心工具包
$ sudo yum -y install git-core
```

#### Windows 平台上安装

安装包下载地址：[http://msysgit.github.io/](http://msysgit.github.io/)
* 下载并运行安装文件

![Git Setup](http://www.runoob.com/wp-content/uploads/2015/02/20140127131250906)
* 安装完成后，使用命令行的 **Git Bash** 工具（已经自带了 SSH 客户端）
* 另外还有一个图形界面的 Git 项目管理工具，在开始菜单里找到"**_Git_**"->"**_Git Bash_**"，会弹出 Git 命令窗口，你可以在该窗口进行 Git 操作。

#### Mac 平台上安装
安装包下载地址：[http://sourceforge.net/projects/git-osx-installer/](http://sourceforge.net/projects/git-osx-installer/)

![Install Git Installer](http://www.runoob.com/wp-content/uploads/2015/02/18333fig0107-tn.png)

---

## Git 配置

**Git** 提供了一个叫做 _git config_ 的工具，专门用来配置或读取相应的工作环境变量。
这些环境变量，决定了 **Git** 在各个环节的具体工作方式和行为。这些变量可以存放在以下三个不同的地方：
* _/etc/gitconfig_ 文件：系统中对所有用户都普遍适用的配置。若使用 `git config` 时用 `--system` 选项，读写的就是这个文件。
* _~/.gitconfig_ 文件：用户目录下的配置文件只适用于该用户。若使用 `git config` 时用 `--global` 选项，读写的就是这个文件。
* 当前项目的 Git 目录中的配置文件（也就是工作目录中的 _.git/config_ 文件）：这里的配置仅仅针对当前项目有效。每一个级别的配置都会覆盖上层的相同配置，所以 _.git/config_ 里的配置会覆盖 _/etc/gitconfig_ 中的同名变量。

在 Windows 系统上，Git 会找寻用户主目录下的 _.gitconfig_ 文件。主目录即 _$HOME_ 变量指定的目录，一般都是 _C:\Documents and Settings\$USER_。

此外，Git 还会尝试找寻 _/etc/gitconfig_ 文件，只不过看当初 Git 装在什么目录，就以此作为根目录来定位。

#### 用户信息

> `git config --global [user.name|user.email] (content)`

``` shell
# 配置用户名
# 全局用户名
$ git config --global user.name "anton"

# 配置邮箱
# 全局邮箱
$ git config --global user.email 1176465592@qq.com
```

如果 **使用** 了 `--global` 选项，那么更改的配置文件就是位于你用户主目录下的那个，以后你所有的项目都会默认使用这里配置的用户信息。

如果要在某个特定的项目中使用其他名字或者电邮，只要 **去掉** `--global` 选项重新配置即可，新的设定保存在当前项目的 _.git/config_ 文件里。

#### 文本编辑器
> `git config --global core.editor emacs`

---

## Git 常用命令

#### 查看版本号
> `git --version`

``` shell
$ git --version
git version 2.13.1.windows.2
```
