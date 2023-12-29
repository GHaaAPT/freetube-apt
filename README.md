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
75a4441b8a5ec3cf5937fa867391554dad6bf118a99496af1dfc6b8dc2437ef6  pool/main/f/freetube/freetube_0.19.1_amd64.deb  
11a6a364c9182688bab210f0ec09c302dd60074f66bc8b8352e285016549ca27  pool/main/f/freetube/freetube_0.19.1_arm64.deb  
11a6a364c9182688bab210f0ec09c302dd60074f66bc8b8352e285016549ca27  pool/main/f/freetube/freetube_0.19.1_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
