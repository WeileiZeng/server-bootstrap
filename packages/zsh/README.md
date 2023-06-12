ref:

https://stackoverflow.com/questions/15293406/install-zsh-without-root-access


Steps to install without root
```
wget -O zsh.tar.xz https://sourceforge.net/projects/zsh/files/latest/download
tar -xf zsh.tar.xz
./configure --prefix=/home/weileizeng/.local
make && make install
```

add the following in `.bash_profile` to make zsh the default shell
```
#.bash_profile
#set zsh as default
[ -f $HOME/bin/zsh ] && exec $HOME/bin/zsh -1
```


install oh my zsh
```
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

ref:
https://gist.github.com/ZhaofengWu/f345652e994e3b68c309352a7610460f