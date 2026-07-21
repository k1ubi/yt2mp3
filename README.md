<div align="center">

```
__   _______ _____ ___  _________ _____ 
\ \ / /_   _/ __  \|  \/  || ___ \____ |
 \ V /  | | `' / /'| .  . || |_/ /   / /
  \ /   | |   / /  | |\/| ||  __/    \ \
  | |   | | ./ /___| |  | || |   .___/ /
  \_/   \_/ \_____/\_|  |_/\_|   \____/ 
```

`[ one link in, one mp3 out ]`

![bash](https://img.shields.io/badge/BASH-ff00c8?style=for-the-badge&logo=gnubash&logoColor=00fff9&labelColor=0a0014)
![youtube--dl](https://img.shields.io/badge/YOUTUBE--DL-00fff9?style=for-the-badge&logo=youtube&logoColor=0a0014&labelColor=0a0014)

</div>

<br>

```
▓▒░ 0x00 // WHAT IT DOES ░▒▓
```

`yt2mpt.sh` is a light wrapper around [`youtube-dl`](https://github.com/ytdl-org/youtube-dl): it
prompts for a link, then extracts the audio at max quality and converts it straight to mp3. That's
the whole tool — no arguments to memorize, no config file.

<br>

```
▓▒░ 0x01 // LOADOUT ░▒▓
```

- `python3 -m pip install youtube-dl` (the script calls `youtube-dl` directly, so it must be on `PATH`)

<br>

```
▓▒░ 0x02 // RUN IT ░▒▓
```

```console
root@node:~/yt2mp3# chmod +x yt2mpt.sh
root@node:~/yt2mp3# ./yt2mpt.sh
##############################################
#   This is a Youtube to mp3 downloader      #
##############################################

Insert the link to start from:
> https://www.youtube.com/watch?v=...

Starting...
```

Under the hood it runs:

```console
youtube-dl --extract-audio --audio-format mp3 --audio-quality 0 --rm-cache-dir $ytlink
```

`--audio-quality 0` = best available, `--rm-cache-dir` clears youtube-dl's cache before each pull.

<br>

<div align="center">

`.: . . : <[ your audio, extracted ]> : . : .`

</div>
