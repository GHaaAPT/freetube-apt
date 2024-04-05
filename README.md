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
5a848ff7a9e77a1d285954bf9821fe16021a13180fac852913602936592a7fe2  pool/main/f/freetube/freetube_0.20.0_amd64.deb  
25efcea433e0e6d0e1995746e01e2d1af0763bb69a4d8640f33d8680ad659afa  pool/main/f/freetube/freetube_0.20.0_arm64.deb  
f3f4f03b725a33b7b4712d1d0e1119262587cd6cb2ac634d1d2619e323eacd3d  pool/main/f/freetube/freetube_0.20.0_armhf.deb  


# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
