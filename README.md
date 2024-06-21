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
c010e55a608bcee817f969a02ab3d9cf4368696f4a2b954c6adebc4e0b70868a  pool/main/f/freetube/freetube_0.21.0_amd64.deb  
eafbf46bf0b1768030d8fd83ac99a0c3b907e84bb3b60a9aae5a40f722895ebc  pool/main/f/freetube/freetube_0.21.0_arm64.deb  
63bf303f5987716ee3a4c920466361acc5b8c28ec9648df99ae30fd544d65a09  pool/main/f/freetube/freetube_0.21.0_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
