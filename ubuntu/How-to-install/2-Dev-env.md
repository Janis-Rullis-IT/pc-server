# How to setup my dev env?

## Install

```shell
sudo usermod -a -G www-data root
sudo locale-gen "lv_LV.UTF-8"
sudo apt-get install mc htop git git-cola gedit shutter retext -y
sudo apt-get install software-properties-common
sudo apt-get update
```

## Set shortucts

* Go to 'Settings\Keyboard'.
* Switch to the 'Application Shortucts'.
* Click on 'Add'.

### Commands

* `retext` - F1
* `exo-open --launch FileManager` - Windows + E


## [Configure GIT](https://github.com/janis-rullis/dev/tree/master/git#configure-git)

## Setup shell helpers / shortcuts

```shell
git clone https://github.com/janis-rullis/shell-scripts
cd shell-scripts
sudo cp mdpr.sh  /usr/local/bin/mdpr
sudo cp gits.sh  /usr/local/bin/gits
sudo cp gitd.sh  /usr/local/bin/gitd
sudo cp gitp.sh  /usr/local/bin/gitp
```

## IDE
* [Netbeans](https://github.com/janis-rullis/dev/blob/master/Code-editor/Netbeans/Setup-and-config-netbeans.md)
* [VS Code](https://github.com/janis-rullis/dev/blob/master/Code-editor/VSCode.md#install)
