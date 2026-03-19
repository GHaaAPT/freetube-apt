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
2b773bba2d9f58daa78fd259de725daa8331405816b542434e9a912294dd4b89  pool/main/f/freetube/freetube_0.23.15_amd64.deb  
21c58aae73e9b37b3a8237d124f62c080f4733f192faf0e29c480d216d443ceb  pool/main/f/freetube/freetube_0.23.15_arm64.deb  
14fef225cf4206de19ea2cc21902c4f63a945a32fd26e8a749f1fcf917a8928f  pool/main/f/freetube/freetube_0.23.15_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
