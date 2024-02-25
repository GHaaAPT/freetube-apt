# freetube-apt
Unofficial APT repository for [FreeTube](https://github.com/FreeTubeApp/FreeTube) that will check for updates regularly

EZ update your FreeTube Debian/Ubuntu client

I do this for myself, but if you want to use it, feel free to audit this repo first and you are strongly recommended to do so.

# Install as APT repo manually
```shell
sudo apt remove freetube # if you installed FreeTube through deb file already, uninstall first.
wget -qO- https://knugihk.github.io/freetube-apt/freetube-archive-keyring.asc | gpg --dearmor | sudo tee /usr/share/keyrings/freetube-archive-keyring.gpg > /dev/null
echo 'deb [signed-by=/usr/share/keyrings/freetube-archive-keyring.gpg] https://knugihk.github.io/freetube-apt/ stable main' | sudo tee /etc/apt/sources.list.d/freetube.list
sudo apt update
sudo apt install freetube -y
```

# Checksum
7919ec77e2a1b5930d9af7e8e2db4b5c3152fcabe90a5c84743242c30313934c  pool/main/f/freetube/freetube_0.19.2_amd64.deb  
6488b8f1a0590f2df44b0984efcd4b7c39abcf87d7849513fa142e951487acc1  pool/main/f/freetube/freetube_0.19.2_arm64.deb  
7de7df677d116f05603798d7b847c7b3d2b59334451385cc6ba75c385d16268c  pool/main/f/freetube/freetube_0.19.2_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
