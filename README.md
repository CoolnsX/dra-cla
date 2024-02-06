
### This script is refactored and now using fzf (make sure it is installed as script now checks for it) for showing menus, if you don't like fzf then you can continue to use old one. I would suggest to try fzf based one.

<p align=center>
<br>
<a href="http://makeapullrequest.com"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
<img src="https://img.shields.io/badge/os-linux-brightgreen">
<img src="https://img.shields.io/badge/os-android-brightgreen"></a>
<br>
<a href="https://github.com/CoolnsX"><img src="https://img.shields.io/badge/maintainer-CoolnsX-blue"></a>
<a href="https://github.com/iamchokerman"><img src="https://img.shields.io/badge/maintainer-iamchokerman-blue"></a>

</p>

A cli to browse and watch Korean Drama, Chinese drama. This tool scrapes the site [asianembed](https://asianembed.io) which is the site dramacool scrapes from.

This tool is modified version of [ani-cli](https://github.com/pystardust/ani-cli) which is anime scraping tool. Feel free to check it out if you need to watch anime.

## Table of Contents
- [Install](#Installation)
  - [Linux](#Linux)
    - [Nix](#Nix)
  - [Android](#Android)
- [Uninstall](#Uninstall)
- [Dependencies](#Dependencies)
- [Disclaimer](./disclaimer.md)

## Install

### Linux

Install dependencies [(See below)](#Dependencies)

```sh
git clone https://github.com/CoolnsX/dra-cla && cd dra-cla
sudo cp dra-cla /usr/local/bin/dra-cla
```

*Note that mpv installed through flatpak is not compatible*

#### Nix

``` shell
nix-shell -p dra-cla
```

### Android

Install termux [(Guide)](https://termux.com/)

```sh
pkg update
pkg install git termux-tools ncurses-utils openssl-tool ffmpeg fzf aria2 -y
git clone https://github.com/CoolnsX/dra-cla && cd dra-cla
cp dra-cla $PREFIX/bin/dra-cla
```

Install mpv-android [(Link)](https://play.google.com/store/apps/details?id=is.xyz.mpv)

For VLC: pass ``` dra-cla -v ```

## Uninstall

* Linux: ```sudo rm /usr/local/bin/dra-cla```
* Android: ```rm $PREFIX/bin/dra-cla```

## Dependencies

- fzf (new)
- grep
- sed
- curl
- openssl
- mpv - Video Player
- aria2 - Download manager
- ffmpeg - m3u8 Downloader
