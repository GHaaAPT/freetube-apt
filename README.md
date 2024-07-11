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
ea2264b9458f9911e3a5000038a09a808b8e872e5df19a36201e319cf3ca3b53  pool/main/f/freetube/freetube_0.21.1_amd64.deb  
e125219e9fa0d8da27de604bd666006640938792a102569ed0834d5b1bb5fc03  pool/main/f/freetube/freetube_0.21.1_arm64.deb  
73c56020ad2634c39e0d0972bab54e6a6be76d5b9f8e0b483d7f156a2a6b3bb3  pool/main/f/freetube/freetube_0.21.1_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
