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
23316475faeb035ef40e1970e61ef53ee06ce6a4dfb12e0ba790f5f92059b9ae  pool/main/f/freetube/freetube_0.22.1_amd64.deb  
13816f8d4f8d87321dbe188f1e293169659636915d10fe4620542e0d676aa07d  pool/main/f/freetube/freetube_0.22.1_arm64.deb  
bb33b2d1b7ecfb1f87b7f82f653ac609b29014b4204ed373f3bb0d82d00a86a3  pool/main/f/freetube/freetube_0.22.1_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
