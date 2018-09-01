# Fix video

## Copy hex header from a working video to the broken one

```shell
sudo apt-get install bless
```

### Find in the HEX editor

* Open search and select `as` to 'Text'.
* Search for 'mdat'.

```
.mdat@"��X�-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------/
```

> This header will be ~ 1 MB large.

## Fix with https://github.com/ponchio/untrunc

```shell
sudo apt-get update
sudo apt-get -y install libavformat-dev libavcodec-dev libavutil-dev unzip g++ wget make nasm zlib1g-dev
sudo wget https://github.com/ponchio/untrunc/archive/master.zip
unzip master.zip
cd untrunc-master
sudo wget https://github.com/libav/libav/archive/v12.3.zip && unzip v12.3.zip
cd libav-12.3
sudo ./configure && make
cd ..
g++ -o untrunc -I./libav-12.3 file.cpp main.cpp track.cpp atom.cpp mp4.cpp -L./libav-12.3/libavformat -lavformat -L./libav-12.3/libavcodec -lavcodec -L./libav-12.3/libavresample -lavresample -L./libav-12.3/libavutil -lavutil -lpthread -lz
./untrunc /home/j/Documents/video-fix/working.mp4 /home/j/Documents/video-fix/1.mp4
```