extra notes for zhejiang light

```shell
# download this repo
wget https://github.com/WeileiZeng/server-bootstrap/archive/refs/heads/main.zip

# install everything into DIR folder
DIR="$HOME/.local"

# optional: add these into .bashrc
export PATH="${PATH}:${HOME}/.local/bin"
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$HOME/.local/lib

#for libevents
./configure --prefix=$HOME/.local CPPFLAGS="-P" --disable-openssl

# for ncurse
./configure --prefix=$HOME/.local CPPFLAGS="-P" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib" --disable-unicode

#for tmux
./configure --prefix=$HOME/.local CPPFLAGS="-P -I$DIR/include/ncurses" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib"

# for htop
./configure --prefix=$HOME/.local CPPFLAGS="-P -I$DIR/include/ncurses" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib" --disable-unicode

#for emacs
./configure --prefix=$HOME/.local --with-gnutls=ifavailable  CPPFLAGS="-P -I$DIR/include/ncurses" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib"
```
