# Yohan Kim's Music
This repository contains a collection of files to help create albums of
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

Alternatively to python/youtube-dl, you can of course also use a service
on the Internet (e.g. https://yt5s.com/) to download the videos.

## Sub folders
As a broad major selection, the music was sorted into a ``Faith`` and a
``Secular`` album in the ``albums`` sub-folder. Each of these album
sub-folders has a mirrored structure, containing

- an ``info`` folder with small text files containing instructions
- a ``lists`` folder containing playlists (orders) for easy listening
- an ``m4a`` folder into which ``.m4a`` files will be downloaded
- an ``mp3`` folder into which ``.mp3`` files can be converted
- an ``orig`` folder into which original ``.m4a`` files can be downloaded

## Implementing the conversion
For music players that support the native audio stream embedded in the
YouTube videos (M4A format), it is sufficient to extract the audio from
the videos using

``ffmpeg -i SOURCE.mp4 -vn -acodec copy <FFMPEG_OPTIONS> TARGET.m4a``

whereas the FFMPEG_OPTIONS can be found in the text files in the ``info``
sub-folder. This cuts off the trailing portion in newer videos (starting
late 2018).

To convert files to MP3 format, you can use

``ffmpeg -i SOURCE.mp4 -vn -ar 44100 -ac 2 -b:a 192k TARGET.mp3``

or

``ffmpeg -i SOURCE.m4a -vn -ar 44100 -ac 2 -b:a 192k TARGET.mp3``

And this can of course be combined into a single step

``ffmpeg -i SOURCE.mp4 -vn -ar 44100 -ac 2 -b:a 192k <FFMPEG_OPTIONS> TARGET.mp3``
