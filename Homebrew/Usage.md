# Homebrew 基本使用

安装一个包，可以简单的运行：
```bash
    $ brew install <package_name>
```
更新 Homebrew 在服务器端上的包目录：
```bash
    $ brew update
```
查看你的包是否需要更新：
```bash
    $ brew outdated
```
更新包：
```bash
    $ brew upgrade <package_name>
```
Homebrew 将会把老版本的包缓存下来，以便当你想回滚至旧版本时使用。但这是比较少使用的情况，当你想清理旧版本的包缓存时，可以运行：
```bash
    $ brew cleanup
```
查看你安装过的包列表（包括版本号）：
```bash
    $ brew list --versions
```