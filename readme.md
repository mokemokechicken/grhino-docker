About
=======
grhino on Mac using Docker.

Requirements
---------

* Mac
* Docker
* Homebrew

How to Use
=========

SETUP
---------
```bash
brew install socat
brew install caskroom/cask/brew-cask
brew cask install xquartz
```

Build Container
--------

```bash
make
```

RUN grhino
------------

```bash
open -a XQuartz
socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"

# open another terminal
IP=<your mac IP>
docker run -it grhino /usr/games/grhino --display=$IP:0
```


