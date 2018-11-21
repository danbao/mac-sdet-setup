# Node.js

使用 Homebrew 安装 [Node.js](http://nodejs.org/):

```bash
    $ brew update
    $ brew install node
```

由于国内的网络问题，所以建议吧npm源设置到[淘宝npm镜像](https://npm.taobao.org/)

```bash
    $ npm config set registry https://registry.npm.taobao.org
```

一般 Node modules 通常被安装在每个项目的本地文件夹 `node_modules`，
但有几个包推荐你安装在全局：

[babel-cli](https://babeljs.io/docs/en/babel-cli)

```bash
    $ npm install babel-cli -g
```

### Npm 使用

安装包:
```bash
    $ npm install <package>     # 安装在本地项目中
    $ npm install -g <package>  # 安装在全局
```
安装包，并且将其保存你项目中的 `package.json` 文件:
```bash
    $ npm install <package> --save
```
查看 npm 安装的内容:
```bash
    $ npm list     # 本地
    $ npm list -g  # 全局
```
查看过期的包（本地或全局）:
```bash
    $ npm outdated [-g]
```
更新全部或特别指定一个包:
```bash
    $ npm update [<package>]
```
卸载包:
```bash
    $ npm uninstall <package>
```