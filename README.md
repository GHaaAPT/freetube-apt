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
9bee4f73cebbd5c095ae9099981c1cab39378df7f2c471d6f5dc02f106b8ab91  pool/main/f/freetube/freetube_0.21.2_amd64.deb  
177a3333206cbf2b03208176d733876f81c51f0b5cde3b86a519f9d5f9d0d600  pool/main/f/freetube/freetube_0.21.2_arm64.deb  
47e23d500c5bc3371f1ef2a1dd57b216bca130040e62a9f40d2237251469dfc6  pool/main/f/freetube/freetube_0.21.2_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
