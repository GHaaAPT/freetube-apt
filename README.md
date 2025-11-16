# freetube-apt
Unofficial APT repository for [FreeTube](https://github.com/FreeTubeApp/FreeTube) that will check for updates regularly

EZ update your FreeTube Debian/Ubuntu client

I do this for myself, but if you want to use it, feel free to audit this repo first and you are strongly recommended to do so.

# Install as APT repo manually
```shell
sudo apt remove freetube # if you installed FreeTube through deb file already, uninstall first.
wget -qO- https://ghaaapt.github.io/freetube-apt/freetube-archive-keyring.asc | gpg --dearmor | sudo tee /usr/share/keyrings/freetube-archive-keyring.gpg > /dev/null
echo 'deb [signed-by=/usr/share/keyrings/freetube-archive-keyring.gpg] https://ghaaapt.github.io/freetube-apt/ stable main' | sudo tee /etc/apt/sources.list.d/freetube.list
sudo apt update
sudo apt install freetube -y
```

# Checksum
0cf6605b489493752946b7bf995a4dbcaf95b8df9f6c42f9ad181ed007ad87b2  pool/main/f/freetube/freetube_0.23.5_amd64.deb  
75a9fe67046f3b0d03da71f7f0f8b86c560f77f7b27bb7fe4d57355edc560e87  pool/main/f/freetube/freetube_0.23.5_arm64.deb  
dfe70b60bf03a6302679c543e9263152a20832c7a7bf4943a4e73267b803ae12  pool/main/f/freetube/freetube_0.23.5_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
