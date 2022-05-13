# Find by filename or content


## sed Tricks
* https://www.tecmint.com/linux-sed-command-tips-tricks/
* https://www.cyberciti.biz/faq/how-to-use-sed-to-find-and-replace-text-in-files-in-linux-unix-shell/

```shell
sed -i 's/db_v2/db_v1/g' tab.sql
```

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
> `model/UsrModel.php:18:		// SHA-512`

### [Grep characters before and after match?](https://stackoverflow.com/a/8101804)

```shell
grep -E -o "John.{0,10}" users.txt
```
> John Doe

## Find by filename

### Contains

```shell
find * -name '*2638*'
```

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
