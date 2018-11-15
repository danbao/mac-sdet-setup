# Homebrew Cask

你已经感受到了使用 Homebrew 安装命令行程序的便利。那么接下来，我们将通过 Homebrew Cask 优雅、简单、快速的安装和管理 OS X 图形界面程序，比如 Google Chrome。

### 安装

安装 Homebrew-cask 是如此的简单直接,因为最新版的brew已经集成了brew cask，所以直接运行以下命令即可完成：

    $ brew cask install google-chrome // 安装 Google 浏览器
    $ brew update && brew upgrade brew-cask && brew cleanup // 更新

### 搜索

如果你想查看 cask 上是否存在你需要的 app，可以到 [caskroom.io](http://caskroom.io/) 进行搜索。

### 文件预览插件

有些 [插件](https://github.com/sindresorhus/quick-look-plugins) 可以让 Mac 上的文件预览更有效，比如语法高亮、markdown 渲染、json 预览等等。

```bash
    $ brew cask install qlcolorcode
    $ brew cask install qlmarkdown
    $ brew cask install quicklook-json
    $ brew cask install quicklook-csv
    $ brew cask install betterzipql
```

### OS X 图形界面程序

```bash
    $ brew cask install cheatsheet
    $ brew cask install dropbox
    $ brew cask install google-chrome
```
---
`注：`
并不喜欢 brew cask 的安装方式，更倾向于到 App Store 或官方下载 OS X 图形界面程序。主要因为名字不好记忆、偶尔需要手动更新，另外当你使用 Alfred 或 Spotlight ，你将发现将程序安装在 ~/Application 会很方便。

