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
bf8649c7b384cd50178d6c887371472916bfdacb9971e939c35ddbe4ab3adc08  pool/main/f/freetube/freetube_0.21.3_amd64.deb  
255eae1ad5603e718a50e6b08be1e33dfef63b6d2efc9dfe1141d56a87c3effc  pool/main/f/freetube/freetube_0.21.3_arm64.deb  
1da3f8bc38098b541d36d394e5c5f189c7b5e7f9e32ee4a45c4715eeb2c25bad  pool/main/f/freetube/freetube_0.21.3_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
