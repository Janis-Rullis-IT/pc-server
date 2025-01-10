# [Install ubuntu on encrypted partitions](https://medium.com/@chrishantha/encrypting-disks-on-ubuntu-19-04-b50bfc65182a)

This is done in the live USB env, **before** installing the OS.

## In Gparted
> 250gb disk.
Create a `gpt` partition table first. These are the correct partitions (not sure about swap). /efi and stuff is configured in the later installation step.

* boot / Boot / 1 GB / prim / ext4
* swap / Swap / 4 GB / prim / ext4
* root / Root / 60 GB / prim / ext4 - will later mapped to `/dev/mapper/vgroot-lvroot`.
* home / Home / 140> GB / prim / ext4 - will later mapped to `/dev/mapper/vghome-lvhome`.

## Encrpypt

sudo cryptsetup luksFormat --hash=sha512 --key-size=512 /dev/nvme0n1p8
sudo cryptsetup open --type=luks /dev/nvme0n1p8 rootfs

sudo cryptsetup luksFormat --hash=sha512 --key-size=512 /dev/nvme0n1p6
sudo cryptsetup open --type=luks /dev/nvme0n1p6 home

## Create volumes

sudo pvcreate /dev/mapper/rootfs
sudo vgcreate vgroot /dev/mapper/rootfs
sudo lvcreate -n lvroot -l 100%FREE vgroot

sudo pvcreate /dev/mapper/home
sudo vgcreate vghome /dev/mapper/home
sudo lvcreate -n lvhome -l 100%FREE vghome

## Install with manual partitions

* Then Continue Testing.

## Collect UUIDs

sudo blkid /dev/nvme0n1p8
sudo blkid /dev/nvme0n1p6

## Mount

sudo mount /dev/mapper/vgroot-lvroot /mnt
sudo mount /dev/nvme0n1p5 /mnt/boot
sudo mount /dev/mapper/vghome-lvhome /mnt/home
sudo mount --bind /dev /mnt/dev

## Chroot

sudo chroot /mnt

mount -t proc proc /proc
mount -t sysfs sys /sys
mount -t devpts devpts /dev/pts

## Create the crypttab file

sudo nano /etc/crypttab

# <target name> <source device> <key file> <options>
rootfs UUID=<ROOT_UUID> none luks,discard
home  UUID=<HOME_UUID> none luks,discard

## Update, refresh the kernel

update-initramfs -k all -c

## Reboot

* Now the ubu login with 'Unlock drive' password request should appear.
****
