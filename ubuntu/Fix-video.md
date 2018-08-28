# Fix video

## Copy hex header from a working video to the broken one

```
.mdat@"��X�-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------/
```


```shell
sudo apt-get install bless
```

## Fix with https://github.com/ponchio/untrunc

```shell
apt-get update
apt-get -y install libavformat-dev libavcodec-dev libavutil-dev unzip g++ wget make nasm zlib1g-dev
wget https://github.com/ponchio/untrunc/archive/master.zip
unzip master.zip
cd untrunc-master
wget https://github.com/libav/libav/archive/v12.3.zip && unzip v12.3.zip
cd libav-12.3
./configure && make
cd ..
g++ -o untrunc -I./libav-12.3 file.cpp main.cpp track.cpp atom.cpp mp4.cpp -L./libav-12.3/libavformat -lavformat -L./libav-12.3/libavcodec -lavcodec -L./libav-12.3/libavresample -lavresample -L./libav-12.3/libavutil -lavutil -lpthread -lz
./untrunc /home/j/Documents/video-fix/working.mp4 /home/j/Documents/video-fix/1.mp4
```