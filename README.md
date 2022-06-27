# Yohan Kim's Music
This repository contains a collection of files to generate albums of
[Yohan Kim's music](http://youtube.com/c/YohanKimMusic/videos).

## Support for Yohan Kim
If you enjoy Yohan's music, please consider subscribing to his
[Patreon account](https://www.patreon.com/yohankimmusic), offering
additional "behind the scenes" videos, instructional material, and so
much more! :)

## Requirements
To download and process the YouTube links given in the ``*.info`` files
in the ``info`` sub-folders, the following software is required:

- python (to run the scripts)
- [youtube-dl](https://youtube-dl.org/)
- [ffmpeg](https://ffmpeg.org/)

## Sub folders
As a broad major selection, the music was sorted into a ``Faith`` and a
``Secular`` album in the ``albums`` sub-folder. Each of these album
sub-folders has a mirrored structure, containing

- an ``info`` folder with small text files containing instructions
- a ``lists`` folder containing playlists (orders) for easy listening
- an ``m4a`` folder into which ``.m4a`` files will be downloaded
- an ``mp3`` folder into which ``.mp3`` files can be converted
- an ``orig`` folder into which original ``.m4a`` files can be downloaded

The ``bin`` folder contains python scripts for downloading the initial
``.m4a`` files into the ``m4a`` sub-folders. Upon request, MP3 versions
can be converted from these files. Also, versions of original recordings
can be downloaded (for comparison).
