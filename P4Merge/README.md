# P4Merge

P4Merge是Git的一个第三发Diff和Merge工具(可视化冲突解决工具),免费且支持中文,有Mac和Windows版

### 下载
打开这个链接: [P4Merge Download](https://www.perforce.com/zh-hans/perforce/product/10)，在`FAMILY`下拉框选择`Macintosh` ，点蓝色的 `Download`，选择跳过 `Skip Registration` ，就会开始下载了。
下载到`P4V.dmg`文件后，双击打开，拖动其中的`p4merge`到`Application`文件夹上就可以完成安装了。

### 配置

如果是想在命令行的git对比文件,需要做如下设置
```bash
git config --global diff.tool p4merge
git config --global difftool.p4merge.cmd /Applications/p4merge.app/Contents/MacOS/p4merge
git config --global difftool.p4merge.cmd "/Applications/p4merge.app/Contents/Resources/launchp4merge \$LOCAL \$REMOTE"
git config --global difftool.p4merge.path "/Applications/p4merge.app/Contents/Resources/launchp4merge"
```
以后想要比较Git中的代码时，敲git difftool filepath 即可

如果是想在SourceTree中对比,需要如下配置
点击窗口左上角的** SourceTree > Perferences > Diff **
在`External Diff / Merge` Tab 中把`Visual Diff Tool`和`Merge Tool`的选项都改为`P4Merge`就可以了