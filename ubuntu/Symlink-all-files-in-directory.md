# [Symlink all files from a base directory to a target directory](http://www.commandlinefu.com/commands/view/1225/symlink-all-files-from-a-base-directory-to-a-target-directory)

`ln -s $PWD/smarty-custom-plugins/* vendor/smarty/smarty/libs/plugins/`

## Beware!

 This command raises `...: File exists` error, if executed multiple times.

### How to avoid?

If You can, then use the copy command `cp` with argument `-u` that overwrites
only if the source is newer.

`cp -u $PWD/smarty-custom-plugins/* vendor/smarty/smarty/libs/plugins/"`