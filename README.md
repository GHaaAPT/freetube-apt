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
e30a9e4f0bb0887d0691f5479e04963f8d9aec8d232f9d1cef6577b8af1a50ab  pool/main/f/freetube/freetube_0.25.1_amd64.deb  
44ec8f3550a0e9a0610be5a0b66ce91ee7fb44aef0483189436a1e9d98ae19f5  pool/main/f/freetube/freetube_0.25.1_arm64.deb  
e64e4e6cbc9537a71c796e60cdf943e799b16b53513b6aea84454287ba792d9a  pool/main/f/freetube/freetube_0.25.1_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
