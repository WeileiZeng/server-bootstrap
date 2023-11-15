extra notes for zhejiang light

```shell
# download this repo
wget https://github.com/WeileiZeng/server-bootstrap/archive/refs/heads/main.zip


DIR="$HOME/.local"
export PATH="${PATH};/home/export/online1/aiuser/zj_zhengwl/.local/bin"


# for ncurse
./configure --prefix=$HOME/.local CPPFLAGS="-P" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib" --disable-unicode

#for tmux
./configure --prefix=$HOME/.local CPPFLAGS="-P -I$DIR/include/ncurses" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib"
```
