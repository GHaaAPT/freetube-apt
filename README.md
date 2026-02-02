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
c7e9371a794cdc4e065471bb19b424bc36f20f3531b9d8c0b6f25e21f5db14f7  pool/main/f/freetube/freetube_0.23.13_amd64.deb  
96a89fbb99c1ed9b4aababac8fc8f209aa7e0c3a582b6e652c69edaae46a564c  pool/main/f/freetube/freetube_0.23.13_arm64.deb  
0d8260c96110934bdc677bfe6bb29341b65ec4d409eda1d81c7a0fb1bb0348e1  pool/main/f/freetube/freetube_0.23.13_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
