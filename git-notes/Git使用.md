# Git 使用

### 配置用户信息
``` bash
# git 用户数据初始化
#   --global 全局配置
git config --global user.name "name"
git config --global user.email example@email.com
```

### 初始化
``` bash
# git 初始化本地仓库
#   [dir-path] 可选，指定详细路径
git init [dir-path]
```

### 克隆仓库
``` bash
# 从本地克隆分支
#   [dir-path] 必填，用于指定详细路径
git clone [dir-path]

# 从远程端克隆分支到本地
#   username  用户名
#   host      主机名或IP地址
#   [dir-path] 必填，用于指定详细路径
git clone username@host [dir-path]
```

### 仓库操作
``` bash
# 添加代码到仓库
#   * 当前所有目录和文件
#   . 当前目录
git add [*|.]

# 从资源库中删除文件
#   filename 具体的文件名
git rm [filename|.|*]

# 提交并附加说明
git commit -m '说明'

# 修改最后一次提交的附加说明（vim 操作）
# 进入界面后按 i 可对文本进行编辑
# 修改完成以后按 ESC 退出
# 并输出英文冒号 : ，输入 wq 回车即可保存
#     :wq
git commit -amend
```

### 远程仓库操作
``` bash
# 查看远程连接名
#
#   可选参
#   [
#     -v        查看远程仓库连接
#     add       添加远程仓库连接
#     remove    删除远程仓库连接
#     set-url   设置远程仓库连接
#   ]
#   [remote-name] 远程连接名
#   [url] 远程连接
git remote [-v|add|remove|set-url] [remote-name] [url]

# 查看远程连接
git remote -v

# 添加远程仓库 URL 连接
#   [remote-name] 远程连接名
#   [url] 远程连接
git remote add [remote-name] [url]

# 删除远程分支
#   [remote-name] 远程连接名
git remote remove [remote-name]

# 重新设置远程分支 URL 连接
#   [remote-name] 远程连接名
#   [url] 远程连接
git remote set-url [remote-name] [url]
```

### 抓取数据
``` bash
# 从远程抓取数据到本地
#   [remote-name] 远程连接名
git fetch [remote-name]
```

### 提交代码库
``` bash
# 提交分支
#   [remote-name] 远程连接名
#   [branch-name] 分支名
#   [--allow-unrelated-histories] 兼容旧版本（用于2.9版本以上）
git pull [remote-name] [branch-name] [--allow-unrelated-histories]
```

### 合并代码库
``` bash
# 合并分支
#   [remote-name] 远程连接名
#   [branch-name] 分支名
git push -u [remote-name] [branch-name]
```

### 创建分支
``` bash
# 创建分支
#   [branch-name] 分支名
git branch [branch-name]
```

### 交换分支
``` bash
# 切换分支
#   [branch-name] 分支名
git checkout [branch-name]
```
