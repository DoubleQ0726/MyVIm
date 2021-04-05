# MyVim
set vim and vim configure

**环境**

```c++
g++ (Ubuntu 9.3.0-17ubuntu1~20.04) 9.3.0
cmake version 3.16.3
Python 3.8.5
VIM - Vi IMproved 8.1 (2018 May 18, compiled Apr 15 2020 06:40:31)
```

#### Just For Linux

##### 1. 建立文件

在用户目录下新建文件夹`.vim`，然后再`.vim`中建立`vim`配置文件`vimrc`。

##### 2. 下载插件管理器

使用`vim-plug`来管理`vim`插件。

`github`地址[https://github.com/junegunn/vim-plug](https://github.com/junegunn/vim-plug)

执行以下命令进行安装

```C++
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

基本示例

```c++
call plug#begin()
Plug 'tpope/vim-sensible'
call plug#end()
```

**安装插件**

在`Normal`模式下输入`: PlugInstall`即可

##### 3. 常用插件

对于C/C++的代码提示及跳转采用[YCM](https://github.com/ycm-core/YouCompleteMe)插件。

**前置安装命令**

```c++
sudo apt install build-essential cmake vim-nox python3-dev
```

**C/C++所需Clang**

```c++
sudo python3 install.py --clangd-completer
```

**编译`YCM`插件**

```
cd ~/.vim/plugged/YouCompleteMe
sudo python3 ./install.py
```

**将系统头文件包含到文件`.ycm_extra_conf.py`**

文件内容不同版本系统需要注意更换版本号(此处为9)，因为`g++ (Ubuntu 9.3.0-17ubuntu1~20.04) 9.3.0`

```
cd ~/.vim
vim .ycm_extra_conf.py
```



以上`vimrc`与`.ycm_extra_conf.py`文件内容可以直接下载使用。

