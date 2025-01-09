# [Get a full info about a sys](https://www.tecmint.com/commands-to-collect-system-and-hardware-information-in-linux/)

## os

```shell
cat /etc/os-release 
```
```
NAME="Alpine Linux"
ID=alpine
VERSION_ID=3.12.7
PRETTY_NAME="Alpine Linux v3.12"
HOME_URL="https://alpinelinux.org/"
BUG_REPORT_URL="https://bugs.alpinelinux.org/"
```

```shell
uname -a > os.txt
```
> Linux tecmint.com 3.13.0-37-generic #64-Ubuntu SMP Mon Sep 22 21:28:38 UTC 2014 x86_64 x86_64 x86_64 GNU/Linux


```shell
mkdir sys-info
cd sys-info
```

## hw

```shell
sudo lshw -html > sys.html
```

## Video card
```shell
lspci
```
> Then check for VGA devices. Example, `Advanced Micro Devices, Inc. [AMD/ATO] Ellesmere [Radeon RX 470/480 ...`.

## bios

```shell
sudo dmidecode -t bios > bios.txt
```

## fs

```shell
sudo fdisk -l > fs.txt
```

## sys

```shell
sudo dmidecode -t system > sys2.txt
```

## cpu

```shell
lscpu > cpu.txt
```

```shell
sudo dmidecode -t processor > cpu2.txt
```

## partitions

```shell
lsblk -a > part.txt
```

## mem

```shell
sudo dmidecode -t memory > mem.txt
```

## sata

```shell
sudo hdparm /dev/sda1
```

## usb

```shell
lsbusb
```

## pci

```shell
lspci -v
```

## sys name

```shell
uname
```
> Linux

## net hostname

```shell
uname -n
```
> local.test

## kernel v

```shell
uname -k
```
> 64-Ubuntu SMP Mon Sep 22 21:28:38 UTC 2014

## kernel release

```shell
uname -r
```
> 3.13.0-37-generic

## hw name

```shell
uname -m
```
> x86_64
