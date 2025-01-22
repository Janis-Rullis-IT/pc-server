# 1-Dev-env.md

sudo apt update && sudo apt upgrade
sudo apt install git mc gedit partitionmanager
sudo apt install vlc meld htop git-cola shutter
ssh-key-gen
cat ~/.ssh/id_...pub
dpkg -i chrome....deb
dpkg -i code....deb

sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
getent group docker
sudo usermod -aG docker j
