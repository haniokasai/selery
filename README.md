![SEL Logo](https://i.imgur.com/cTu1FE5.png)

**A Server for Minecraft (Bedrock Engine) and Minecraft: Java Edition written in [D](https://dlang.org)**

[![Join Chat](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/sel-project/Lobby)
[![Build Status](https://travis-ci.org/sel-project/selery.svg?branch=master)](https://travis-ci.org/sel-project/selery)
[![Build status](https://ci.appveyor.com/api/projects/status/k92u01kgy09rbwmm?svg=true)](https://ci.appveyor.com/project/Kripth/selery)

The server is still in development and some features are not supported yet.

Supported Minecraft versions:
- 1.1.*
- 1.2 beta

Supported Minecraft: Java Edition versions:
- 1.10.*
- 1.11.*
- 1.12.*

### Structure

SEL is based on the [hub-node communication protocol](https://sel-utils.github.io/protocol/hncom), which means that it can run as two separate instances (hub and node), which are connected through a socket.

## Create a server

:warning: does not work with DMD >2.074

:warning: doesn't compile using 32-bit DMD

:warning: doesn't work using DMD in release mode

```
git clone git://github.com/sel-project/selery
cd selery/builder
dub --single init.d
dub build
cd ..
./selery-default [-edu] [-realm]
```

If you're on Windows you must compile using a 64-bit architecture (for example `dub build -a x86_64`)
