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
b2f87f5e4ad1285b5004ea0028000edf0c4fba94ffab292a84cfebb196fbaa84  pool/main/f/freetube/freetube_0.25.0_amd64.deb  
c0e5b2659604d7f1a8ebf7de9c9fdaff57965f358380819b305f19f8b23abbd2  pool/main/f/freetube/freetube_0.25.0_arm64.deb  
376b057352985e99d2c2520773f3645be912c59b8a2d5ff270b62adf0114eb7b  pool/main/f/freetube/freetube_0.25.0_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
