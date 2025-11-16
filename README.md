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
a330ec57bf96822fd4bd8a2675a00e919c932adefe04a09eda1ba8b9d79e3046  pool/main/f/freetube/freetube_0.23.12_amd64.deb  
9e162e5c8611485a85c3896541bc2c74c822063ce25e303d912e93c65750addb  pool/main/f/freetube/freetube_0.23.12_arm64.deb  
4e2d3353d649bfe04c04e7637af8198fc5c156f90d745335f39fe958ad75f221  pool/main/f/freetube/freetube_0.23.12_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
