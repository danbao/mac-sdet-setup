# Zsh

Linux/macOS下默认的是bash，虽然bash的功能已经很强大，但对于以懒惰为美德的程序员来说，`bash`的提示功能不够强大，界面也不够炫，并非理想工具。
而zsh的功能极其强大，只是配置过于复杂，起初只有极客才在用。后来，有个穷极无聊的程序员可能是实在看不下去广大猿友一直只能使用单调的bash, 于是他创建了一个名为`oh-my-zsh`的开源项目。
`zsh`的所有参数配置都在`~/.zshrc`，我们将另外新建个`env.sh` 文件用于维护别名（aliases），输出（exports）和路径改变（path changes）等等，以免影响 `~/.zshrc`。

### Zsh

安装 oh-my-zsh 让 zsh 获得拓展功能和主题
```bash
    $ curl -L https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh | sh
```
用文本编辑器或 vim 打开 `.zshrc` 进行以下编辑:
```bash
    ZSH_THEME=agnoster
    alias zshconfig="vi ~/.zshrc"
    alias envconfig="vi ~/Projects/config/env.sh"
    plugins=(git colored-man colorize github jira vagrant virtualenv pip python brew osx zsh-syntax-highlighting)
```

用文本编辑器或 vim 打开 `~/Projects/config/env.sh` 进行以下编辑:
```bash
    #!/bin/zsh

    # PATH
    export EDITOR='vim -w'
    # export PYTHONPATH=$PYTHONPATH
    # export MANPATH="/usr/local/man:$MANPATH"

    # Virtual Environment
    export WORKON_HOME=$HOME/.virtualenvs
    export WORKSPACE=$HOME/source

    # FileSearch
    function f() { find . -iname "*$1*" ${@:2} }
    function r() { grep "$1" ${@:2} -R . }

    #mkdir and cd
    function mkcd() { mkdir -p "$@" && cd "$_"; }

    # Aliases
    alias cppcompile='c++ -std=c++11 -stdlib=libc++'
```

---
`注：`

如果是新增环境变量或者是修改环境变量的值，都需要执行 `source ~/.zshrc` 一下才能立即生效。
如果是删除一个环境变量，必须输入 exit 以 logout 当前 shell ，然后再重新打开一个新的 shell 并 login 才能生效。


