# CMake YouCompleteMe Installation

## Dependencies

Make sure the [ack](https://github.com/beyondgrep/ack3) and [ctags](https://github.com/universal-ctags/ctags) packages are install on your system:

    $ sudo pacman -S ack ctags

Also install YCM dependencies:

```
# Arch
$ sudo pacman -S base-devel python clang llvm

# Debian and Ubuntu
$ sudo apt install build-essential python3-dev llvm-defaults

# Fedora 
$ sudo dnf install gcc-c++ make python3-devel clang clang-tools-extra
```

## Installing Plug-ins

Firstly copy the `vimrc` file to your home directory to replace your current `.vimrc` file: 

    $ cp -f ./cmake-ycm/vimrc ~/.vimrc

Make sure the [Vundle](https://github.com/VundleVim/Vundle.vim) plug-in manager is installed on your system. If it's not, run the following commands:

    $ cd ~/.vim
    $ mkdir bundle && cd bundle
    $ git clone https://https://github.com/VundleVim/Vundle.vim Vundle.git
    $ cd ~

Install the plug-ins by running the following on the command-line:

    $ vim +PluginInstall +qall

Vundle will download the required plug-in repositories to the `~/.vim/plugged` directory. 

To complete the YCM installation for CLang:

```
# Clone submodules in downloaded YCM repository
$ git submodule update --init --recursive

# Install YCM
$ python3 install.py --clangd-completer
```

To complete the YCM installation for All:
1. Clone submodules in downloaded YCM repository
```
$ git submodule update --init --recursive
```
2. Install CMake, Vim and Python
```
apt install build-essential cmake vim-nox python3-dev
```
3. Install mono-complete, go, node, java and npm
```
apt install mono-complete golang nodejs openjdk-17-jdk openjdk-17-jre npm
```
4. Compile YCM
```
cd ~/.vim/bundle/YouCompleteMe
python3 install.py --all
```

You will now be able to use the functionality provided by the cmake-ycm configuration next time you launch Vim!

