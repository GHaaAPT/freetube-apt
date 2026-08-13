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
582930fab1a75bf59152d5bd94fd3a238b0f34c8d61ec6c7f317c0fa5bf8266e  pool/main/f/freetube/freetube_0.25.2_amd64.deb  
fdbb085ae15ca9984af58771b241e10817783c18d6228ef7cc92e2fb3cacd5ab  pool/main/f/freetube/freetube_0.25.2_arm64.deb  
403909298ff2a26c62c9d149977531e59ac72d744cbb93c284a9cf349bc06846  pool/main/f/freetube/freetube_0.25.2_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
