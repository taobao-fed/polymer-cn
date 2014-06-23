# 贡献

[polymer 官方讨论区](https://groups.google.com/forum/?fromgroups=#!forum/polymer-dev)，[polymer-cn bug报告](../../issues)

## 贡献原则

* 只做**兼容性修复**，对于官方支持的浏览器上出现的问题，由于可以预见官方会进行修复，我们会保留此bug，不代替官方进行修复，若欲修复此类bug，请参考[官方的贡献文档](https://github.com/polymer/platform/blob/master/CONTRIBUTING.md)；
* 特性检测大于浏览器检测；
* 严格遵循官方代码风格规范；
* 只做最小修复，避免因修复产生其他bug；
* 不要做“看起来好了”的修复，了解问题根本原因后再做修复。

## 搭建贡献平台

1. 安装 Grunt: `sudo npm install -g grunt-cli`
1. 在 github 上 fork 相应的项目并 clone 你的拷贝。
	
	如果 polymer-cn 下还没有 polymer 官方对应的项目，请在 issues 中告诉我们。
	
   > 用你的用户名替换下面的 {{ username }} 和库名称替换下面的 {{ repository }}

        git clone git@github.com:{{ username }}/{{ repository }}.git --recursive

    注意 `--recursive` 。这个参数保证你的 git submodules 正常初始化，如果你没有进行一个递归 clone，你可以自行初始化它们：

        git submodule init
        git submodule update

    下载并执行 `pull-all.sh` 脚本安装兄弟依赖。

        git clone git://github.com/polymer-cn/tools.git && tools/bin/pull-all.sh

1. 测试你的修改
   > 在项目中你做了一些修改，然后执行测试：

        cd $REPO
        npm install
        grunt test

1. 提交代码并提交一个 pull request。

## 提交 pull request

我们迭代的很快！为了避免发生合并冲突，强烈建议在进行修改和提交 pull request 前保持同主项目的同步。最方便的方法就是设置一个叫做 `upstream` 的 remote 并且在进行修改前进行拉取：

    git remote add upstream git://github.com/polymer-cn/{{ repository }}.git

然后在进行修改前，从 upstream 的 `master` 分支拉取：

    git pull upstream master

请将修复提交到 `cn` 分支，在修改前后需要执行的命令是：

    git checkout cn
    git fetch origin -v
    git fetch upstream -v
    git merge upstream/cn
    # make change
    git commit -a -m 'Awesome things.'
    git push

最后，别忘了提交 pull request。
