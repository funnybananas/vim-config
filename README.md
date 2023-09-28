Run following:
```
$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

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

