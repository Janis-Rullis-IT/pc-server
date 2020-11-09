# How to setup my dev env?

## Install

```shell
sudo usermod -a -G www-data root
sudo locale-gen "lv_LV.UTF-8"
sudo add-apt-repository ppa:linuxuprising/shutter
sudo apt-get update
sudo apt-get install mc htop git git-cola gedit shutter meld retext unrar shellcheck libimage-exiftool-perl webp ffmpeg vlc -y
sudo apt-get install software-properties-common
sudo apt-get update
```

# https://linuxhint.com/installing_mysql_workbench_ubuntu/

## Set shortucts

* Go to 'Settings\Keyboard'.
* Switch to the 'Application Shortucts'.
* Click on 'Add'.

### Commands

* `gedit` - F1
* `exo-open --launch FileManager` - Windows + E

## Add the new SSH key to Github / Gitlab

```shell
ssh-keygen
cat ~/.ssh/id_rsa.pub
```

## [Configure GIT](https://github.com/Janis-Rullis-IT/dev/tree/master/Tools/git#configure-git)
## [Set global gitignore](https://github.com/janis-rullis/dev/blob/master/git/Git-ignore/Set-up-global-gitignore.md)
## Setup shell helpers / shortcuts

```shell
cd ~/Desktop
mkdir www
cd www
git clone https://github.com/janis-rullis/shell-scripts
cd shell-scripts
sudo ln -s ~/Desktop/www/shell-scripts/mdpr.sh  /usr/local/bin/mdpr
sudo ln -s ~/Desktop/www/shell-scripts/gits.sh  /usr/local/bin/gits
sudo ln -s ~/Desktop/www/shell-scripts/gitd.sh  /usr/local/bin/gitd
sudo ln -s ~/Desktop/www/shell-scripts/gitp.sh  /usr/local/bin/gitp
sudo ln -s ~/Desktop/www/shell-scripts/res.sh  /usr/local/bin/res
```

## [content_gen](https://github.com/ruu-lv/content_gen)

## IDE

* [Netbeans](https://github.com/Janis-Rullis-IT/dev/blob/master/Tools/Code-editor/Netbeans/Setup-and-config-netbeans.md)
* [VS Code](https://github.com/Janis-Rullis-IT/dev/tree/master/Tools/Code-editor/VSCode#install)

## [Postman](https://github.com/Janis-Rullis-IT/dev/blob/master/Tools/Postman.md)

## [Docker](https://github.com/Janis-Rullis-IT/dev/tree/master/Tools/Docker#install)
