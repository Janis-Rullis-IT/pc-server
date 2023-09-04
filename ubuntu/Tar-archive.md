# Tar archive

* [How to unpack (ungzip, unarchive) a tar.gz file (rebol.com)](http://www.rebol.com/docs/unpack-tar-gz.html)
* [How To Extract .tar.gz Files using Linux Command Line (interserver.net)](https://www.interserver.net/tips/kb/extract-tar-gz-files-using-linux-command-line/)

```shell
tar -czvf stats.tar.gz stats
mkdir stats2
tar -xzvf stats.tar.gz -C stats2
```
