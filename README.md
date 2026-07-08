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
cd08d06694ca97cf1af25229c44b6867175f9fac89244288d9693b775a0d1c6d  pool/main/f/freetube/freetube_0.24.1_amd64.deb  
d82d2162be3eddcbae5653986aff8201b90181dc2daaf00b0dc3606f1b0f1437  pool/main/f/freetube/freetube_0.24.1_arm64.deb  
90352187f9a1d01b8f02b48b822a71e6151d8301cd649384ead0d4a3eddafcde  pool/main/f/freetube/freetube_0.24.1_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
