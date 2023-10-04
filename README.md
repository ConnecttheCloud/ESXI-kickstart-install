# ESXI-kickstart-install

## Esxi automatic installaing using kickstart file from Github 
This document shows how to use kickstart file from github repo and install ESXI on the server. 


## Dependencies 
1) Connected Network & Internet Access (kickstart file is located in Github)
2) Update the config file as required


## Installation Guide 
* Boot esxi from bootable media.
* Press key Shift+O when see it prompted.
* Type the following attribute. It may change the ip address & network setting shoud be changed as corresponding to your environment. 

>`runweasel ks=https://raw.githubusercontent.com/ConnecttheCloud/esxi-kickstart/main/kickstart.cfg ip=10.255.233.20 netmask=255.255.255.0 gateway=10.255.233.1 nameserver=10.255.233.10`

>[!Note]
>Note: kickstart can be sourced at local http server or NFS file share. Just replace https:// to nfs://
>The encrypted root password is generated with openssl cmd `openssl passwd -1 <root_pwd>`

##### 
