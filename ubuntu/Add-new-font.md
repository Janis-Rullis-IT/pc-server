# Add-new-font.md

## Check if installed

```shell
    fc-list | grep -i "Fira"
```
> ''

## Download and copy to the sys

```shell
wget https://github.com/tonsky/FiraCode/releases/download/5.2/Fira_Code_v5.2.zip
unzip Fira_Code_v5.2.zip
sudo cp Fira_Code_v5.2 /usr/share/fonts/. -R
```

## Make sure it is installed

```shell
fc-list | grep -i "Fira"
```

```
/usr/share/fonts/Fira_Code_v5.2/variable_ttf/FiraCode-VF.ttf: Fira Code,Fira Code Light:style=Regular
/usr/share/fonts/Fira_Code_v5.2/ttf/FiraCode-Light.ttf: Fira Code,Fira Code Light:style=Light,Regular
```
