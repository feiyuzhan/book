ffmpeg tutorial


ffmpeg structure
=============

1. libavcodec
2. libavformat
3. libavutil
4. libavfilter
5. libavdevice
6. libswresample
7. libswscale


gcc
=============

compile option :: 
    g++ -I /usr/local/ffmpeg/include delete_file.cpp -L /usr/local/ffmpeg/lib -lavformat -o delete_file.o
    g++ -I /usr/local/ffmpeg/include ffmpeg_list_dir.cpp -L /usr/local/ffmpeg/lib -lavformat -lavutil -o ffmpeg_list_dir.o



log system
=============
1. should include <libavutil/log.h>
2. api:

log ::
    av_log_set_level()
    av_log()



file delete and rename (api : http://www.ffmpeg.org/doxygen/4.1/avio_8h.html)
=============
1. access to file system should include <libavformat/avio.h>

file option ::
    avpriv_io_delete()
    avpriv_io_move()



list_dir
=============

list dir ::
    avio_open_dir()
    avio_open_dir()
    avio_open_dir()



read dic api:
=============


read dic ::
    AVIODirContext : context
    AVIODirEntry : entry 


Some basic struct for ffmpeg:
=============

Basically audio and video are both containers.
Each container has many stream that do not cross over with each other.
each stream is made by serverl packet and there is one or more frame in each packet.
 
* AVFormatContext : show which container is deal with
* AVStream : show which stream is deal with
* AVPacket 


Basic Steps:
=============
demux(解复用) -> get streams -> read packets -> release resources


get meta data of audio and video:
==============

apis :: 
    * av_register_all()
    * avformat_open_input()/ avformat_close_input(); output : AVFormatContext
    * av_dump_format(); output : meta data

e.g:

compile : g++ -I /usr/local/ffmpeg/include mediainfo.cpp -L /usr/local/ffmpeg/lib  -lavutil -lavformat -o mediainfo.o

output::
    Input #0, mov,mp4,m4a,3gp,3g2,mj2, from './1.mp4':
    Metadata:
        major_brand     : isom
        minor_version   : 512
        compatible_brands: isomiso2avc1mp41
        encoder         : Lavf59.10.100
    Duration: 00:00:08.24, bitrate: N/A
    Stream #0:0[0x1](und): Video: h264 (avc1 / 0x31637661), none(tv, bt709), 1920x1080, 3618 kb/s, SAR 1:1 DAR 16:9, 30 fps, 30 tbr, 15360 tbn (default)
        Metadata:
        handler_name    : ISO Media file produced by Google Inc.
        vendor_id       : [0][0][0][0]
    Stream #0:1[0x2](und): Audio: aac (mp4a / 0x6134706D), 44100 Hz, 2 channels, 127 kb/s (default)
        Metadata:
        handler_name    : ISO Media file produced by Google Inc.
        vendor_id       : [0][0][0][0]




    




