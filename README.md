# freetube-apt
Unofficial APT repository for [FreeTube](https://github.com/FreeTubeApp/FreeTube) that will check for updates regularly

EZ update your FreeTube Debian/Ubuntu client

I do this for myself, but if you want to use it, feel free to audit this repo first and you are strongly recommended to do so.

> [!NOTE]
> FreeTube no longer supports ARMv7l builds, so they are no longer distributed in this repository. For details, see [FreeTube's release note](https://github.com/FreeTubeApp/FreeTube/releases/tag/v0.26.0-beta).

# Install as APT repo manually
```shell
sudo apt remove freetube # if you installed FreeTube through deb file already, uninstall first.
wget -qO- https://ghaaapt.github.io/freetube-apt/freetube-archive-keyring.asc | gpg --dearmor | sudo tee /usr/share/keyrings/freetube-archive-keyring.gpg > /dev/null
cat << 'EOF' | sudo tee /etc/apt/sources.list.d/freetube.sources > /dev/null
Types: deb
URIs: https://ghaaapt.github.io/freetube-apt/
Suites: stable
Components: main
Signed-By: /usr/share/keyrings/freetube-archive-keyring.gpg
EOF
sudo apt update
sudo apt install freetube -y
```

# Checksum
b8ae0441283843ada8b6506792cb2c872637a26cd73fffaa2ce19c42e617daa3  pool/main/f/freetube/freetube_0.26.0_amd64.deb  
a1e28c998b64fe682184a864610959425f63a0e8db87d4c290fb0c127aee5093  pool/main/f/freetube/freetube_0.26.0_arm64.deb  

# Copyright
The FreeTube installer (deb file) is re-distributed in AGPLv3
