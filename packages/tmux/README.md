


useful links


- install guide https://gist.github.com/sudkumar/6062def9d56d946b98b6a3853093ee74
- same install guide https://gist.github.com/octavifs/45e120c7abe9bf03c652f70260947344
- download tmux https://github.com/tmux/tmux/wiki
- download ncurse https://invisible-island.net/ncurses/#download_ncurses
- download libevent https://libevent.org/

cmd to build dependency:
```
./configure --prefix=$HOME/.local CPPFLAGS="-P"
make && make install
```

cmd to build tmux (same for htop)
```
DIR="$HOME/.local"
./configure --prefix=$HOME/.local CPPFLAGS="-P" CFLAGS="-I$DIR/include" LDFLAGS="-L$DIR/lib"
make && make install
```

#add path for static libs, e.g. libevent for tmux
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$HOME/.loca/lib