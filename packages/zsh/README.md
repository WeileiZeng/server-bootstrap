ref:

https://stackoverflow.com/questions/15293406/install-zsh-without-root-access


Steps to install without root
```
wget -O zsh.tar.xz https://sourceforge.net/projects/zsh/files/latest/download
tar -xf zsh.tar.xz
./configure --prefix=/home/weileizeng/.local
make && make install
```
