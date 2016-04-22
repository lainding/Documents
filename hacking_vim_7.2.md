# Hacking Vim 7.2

## 定制化Vim
### 配置文件的位置
通常，需要知道的三个配置文件：
* `vimrc`
* `gvimrc`
* `exrc`

`vimrc`文件是Vim的主配置文件。存在两个版本，全局的和个人的。
全局`vimrc`文件放在Vim系统文件安装的文件夹。你可以通过打开Vim并执行在普通模式下执行下面的命令得到。

```vim
:echo $VIM
```
个人`vimrc`文件放在你的主目录下。主目录依赖于操作系统。Vim最初是在Unix系统下，通过前边加一个.号起到隐藏文件的作用，但这在Windows下不起作用。因此`vimrc`文件通过添加一个下划线。

不论在个人`vimrc`中修改的任何内容都将覆盖之前在全局`vimrc`文件中的设置。这样你就可以修改整个配置而无需曾经有访问全局vimrc文件。

你能在普通模式下通过下面的命令找到home目录：
```vim
:echo $HOME
```
在普通模式下通过下面的命令找到你的个人`vimrc`文件
```vim
:echo $MYVIMRC
```

在`vimrc`文件包含`ex`命令，每行一个，而且是默认位置来修改添加到Vim的设置。在本书的其余部分，该文件只是所谓的`vimrc`。

你的`vimrc`文件可以包含外部的配置文件。在`vimrc`文件中，你能使用下面的`source`命令：
```vim
source /path/to/external/file
```
使用这种方法保持`vimrc`文件整洁，和你的配置结构化。

