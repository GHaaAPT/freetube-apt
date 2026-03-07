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
c918041da11592dde2d3336d5441f2eb077878ce59feda04e524b380c853e461  pool/main/f/freetube/freetube_0.23.14_amd64.deb  
34da4e2e0d7631550f3d0d71d3dc3de145f325c3f8048e9809d04605628701f4  pool/main/f/freetube/freetube_0.23.14_arm64.deb  
5a9728ecc363260452f00e3db49ae817880cff8ad26fec5c36252459482dc6a2  pool/main/f/freetube/freetube_0.23.14_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
