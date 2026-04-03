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
ca76930dbd2c7bff1559fa8078958a981c9b18f0eccbd4dd721e3c3d04623452  pool/main/f/freetube/freetube_0.24.0_amd64.deb  
e2dbdbe8f92266a72d388682f3643cd90cc3c1724f50ab0d5365d490621b7edf  pool/main/f/freetube/freetube_0.24.0_arm64.deb  
d26522eab50ece92d34783d027b5857a80871ebc5f40fda3e6d2b88551141ad7  pool/main/f/freetube/freetube_0.24.0_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
