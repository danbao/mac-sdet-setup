# Homebrew

包管理工具可以让你安装和更新程序变得更方便，目前在 OS X 系统中最受欢迎的包管理工具是 [Homebrew](https://brew.sh/).

### 安装

在安装 Homebrew 之前，需要将 **Xcode Command Line Tools** 安装完成，这样你就可以使用基于 Xcode Command Line Tools 编译的 Homebrew。

在 `iTerm` 中复制以下命令（不包括 `$`），跟随指引，将完成 Hombrew 安装。

```bash
    $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
**Cmd+T** 打开一个新的 terminal 标签页，运行以下命令，确保 brew 运行正常。

```bash
    $ brew doctor
```

由于国内的网络问题，建议把Homebrew Bottles源地址设置到[国内镜像源](https://lug.ustc.edu.cn/wiki/mirrors/help/homebrew-bottles)

```bash
    echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zshrc
    source ~/.zshrc
```
---
`注：`

* Homebrew Bottles是Homebrew提供的二进制代码包
* 安装完成后，Homebrew 会将本地 `/usr/local` 初始化为 git 的工作树，并将目录所有者变更为当前所操作的用户，将来 `brew` 的相关操作不需要 sudo 。
