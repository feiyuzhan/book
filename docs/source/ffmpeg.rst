ffmpeg tutorial

=============
ffmpeg structure
=============

1. libavcodec
2. libavformat
3. libavutil
4. libavfilter
5. libavdevice
6. libswresample
7. libswscale

=============
gcc
=============
.. code-block:: 
    g++ -I /usr/local/ffmpeg/include delete_file.cpp -L /usr/local/ffmpeg/lib -lavformat -o delete_file.o


=============
log system
=============
1. should include <libavutil/log.h>
2. api:
.. code-block:: c
    av_log_set_level()
    av_log()


=============
file delete and rename (api : http://www.ffmpeg.org/doxygen/4.1/avio_8h.html)
=============
1. access to file system should include <libavformat/avio.h>
.. code-block:: c
    avpriv_io_delete()
    avpriv_io_move()


=============
dir
=============
.. code-block:: c
    avio_open_dir()
    avio_open_dir()
    avio_open_dir()




