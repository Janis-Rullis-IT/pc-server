# Fix Unable to mount Windows (NTFS) filesystem due to hibernation

* [Unable to mount Windows (NTFS) filesystem due to hibernation (askubuntu.com)](https://askubuntu.com/questions/145902/unable-to-mount-windows-ntfs-filesystem-due-to-hibernation/532753)


```shell
sudo mount -t "ntfs" -o ro /dev/sda4 /media/xubuntu
```