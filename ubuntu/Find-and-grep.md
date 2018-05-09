# Find by filename or content

## Grep - Find by content

* [Grep](https://help.ubuntu.com/community/grep)
* [How do I find all files containing specific text on Linux?](https://stackoverflow.com/a/16957078)

`grep -rnw '/path/to/somewhere/' -e 'pattern'`

-r or -R is recursive,
-n is line number, and
-w stands for match the whole word.
-l (lower-case L) can be added to just give the file name of matching files.

### Example, find 'SHA'
`grep -rn -e "SHA"`

#### Result
`model/UsrModel.php:18:		// SHA-512`


## Find by filename

### Find by extension

 ```bash
find . -name "*.png"

```

## Find in current dir by selecting depth

```shell
find . -maxdepth 1
```

## Ignore directories

```shell
find .  ! -type d
```

## Ignore file

```shell
find . ! -name $file
```

#### [Multiple extensions](https://unix.stackexchange.com/a/15309)

```bash
find ./ -type f \( -iname \*.jpg -o -iname \*.png \)
```
