# [Multi-IPs](https://linuxhint.com/ubuntu_20-04_network_configuration/)

```shell
 sudo gedit /etc/netplan/01-network-manager-all.yaml
 ```
 
 ```yaml
 network:
  version: 2
  renderer: NetworkManager
  ethernets:
   enp9s0:
    dhcp4: no
    addresses:
    - 192.168.88.252/24
    - 192.168.88.253/24
    gateway4: 192.168.88.1
    nameservers:
     addresses: [8.8.8.8, 8.8.4.4]
```

```shell
sudo netplan try
sudo netplan apply
ip a
```

```
2: enp9s0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 70:85:c2:bf:68:01 brd ff:ff:ff:ff:ff:ff
    inet 192.168.88.252/24 brd 192.168.88.255 scope global noprefixroute enp9s0
       valid_lft forever preferred_lft forever
    inet 192.168.88.253/24 brd 192.168.88.255 scope global secondary noprefixroute enp9s0
       valid_lft forever preferred_lft forever
    inet6 fe80::7285:c2ff:febf:6801/64 scope link 
       valid_lft forever preferred_lft forever
```

