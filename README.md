<p align=center>
<br>
<img src="https://img.shields.io/badge/os-linux-orange">
<a href="https://github.com/fengbainuo"><img src="https://img.shields.io/badge/maintainer-fengbainuo-white"></a>

## Table of Contents
- Important information regarding this fork
- [Install](#Install)
  - [Linux](#Linux)
  - Android - unsupported as of now
- [Uninstall](#Uninstall)
- Information about the original tool
- [Disclaimer](./disclaimer.md)

## Important information regarding this fork

As the main project seems to be abandoned for now - given how my pull request to fix the parsed website hasn't been merged since the 28th Nov and the current version doesn't work at all - I'm uploading my changes to the script, so anyone who still wants to keep using it to watch dramas can do so.

Some changes compared to the original one:
- Changed the default player from <i>mpv</i> to <i>VLC</i> (since I use vlc)
- Tested and works with snap VLC (probably works with snap mpv as well)
- No longer outputs the video url in the terminal, since it's mostly necessary only for debugging
- Prints the current server it's using


Things I'm working on/plan to work on:
- Flatpak support
- No check for the default player (currently VLC) if any other supported video player is installed
- Simple install script with dependencies
- Update the android install instructions
- Fuzzy search and other features like seen in [ani-cli](https://github.com/pystardust/ani-cli)

## Install

### Linux

1. Make sure you have all the dependencies installed:
    - grep
    - sed
    - curl
    - openssl
    - aria2 - Download manager
    - ffmpeg - m3u8 Downloader
    - VLC (snap or regular package)

2. Clone the repository

3. Copy the following line to copy the binary to the required directory
    ```bash
    cd dra-cla && sudo cp ./dra-cla /usr/local/bin/dra-cla && cd ..
    ```

4. Optional - delete the cloned directory as it's no longer necessary
    ```bash
    rm -r dra-cla
    ```

### Android - unsupported as of now

Currently not tested with the new website, so it's not supported

## Uninstall

* Run the following command to delete the binary:
    ```bash
    sudo rm /usr/local/bin/dra-cla
    ```

## Information about the original tool

This tool is a fork of CoolnsX's [dra-cla](https://github.com/CoolnsX/dra-cla) (please read the top of this page for more information why this fork was created). From their original README:

>A cli to browse and watch Korean Drama, Chinese drama. This tool scrapes the site [asianembed](https://asianembed.io) which is the site dramacool scrapes from.
<br>
>This tool is modified version of [ani-cli](https://github.com/pystardust/ani-cli) which is anime scraping tool. Feel free to check it out if you need to watch anime.
