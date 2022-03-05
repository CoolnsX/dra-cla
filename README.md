<p align=center>
<br>
<a href="http://makeapullrequest.com"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg"></a>
<img src="https://img.shields.io/badge/os-linux-brightgreen">
<img src="https://img.shields.io/badge/os-android-brightgreen"></a>
<br>
<a href="https://discord.gg/A4c5UWNk"><img src="https://invidget.switchblade.xyz/A4c5UWNk"></a>
<br>
<a href="https://github.com/CoolnsX"><img src="https://img.shields.io/badge/maintainer-CoolnsX-blue"></a>

</p>

A cli to browse and watch Korean Drama, Chinese drama. This tool scrapes the site [dramacool](https://dramacool.fo).

This tool is modified version of [ani-cli](https://github.com/pystardust/ani-cli) which is anime scraping tool. Feel free to checkout if you need to watch anime.

## Table of Contents
- [Install](#Installation)
  - [Linux](#Linux)
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

### Android

Install termux [(Guide)](https://termux.com/)

```sh
pkg install git termux-tools ncurses-utils openssl-tool -y
git clone https://github.com/CoolnsX/dra-cla && cd dra-cla
cp dra-cla $PREFIX/bin/dra-cla
echo 'am start --user 0 -a android.intent.action.VIEW -d "$2" -n is.xyz.mpv/.MPVActivity' > $PREFIX/bin/mpv
chmod +x $PREFIX/bin/mpv
```

Install mpv-android [(Link)](https://play.google.com/store/apps/details?id=is.xyz.mpv)

*Add ```referrer="https://asianembed.io"``` to mpv.conf (Open mpv app, goto three dots top right->Settings->Advanced-->Edit mpv.conf)* 

*Note: VLC android doesn't support referrer option. So it will not work*

## Uninstall

* Other Linux: Just remove the thing from path
* Android: Just remove the thing from path

## Dependencies

- grep
- sed
- curl
- openssl
- mpv - Video Player
- aria2 - Download manager
