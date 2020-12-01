### Install WSL ###

* [link](https://pureinfotech.com/install-windows-subsystem-linux-2-windows-10/)

* Enable Windows Subsystem for Linux 1 (in Windows features)
* Enable Virtual Machine Platform (in PS run: ```Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform```)
* Restart PC
* Download [update](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
* install update
* Set default WSL2 version (in PS run: ```wsl --set-version Ubuntu 2```)
* check version WSL in PS run ```wsl --list --verbose```

---

### Static IP address for WSL (?) ###

* work solution (?): use script:
```
wsl -d Ubuntu-18.04 -u root ip addr add 192.168.50.16/24 broadcast 192.168.50.255 dev eth0 label eth0:1
netsh interface ip add address "vEthernet (WSL)" 192.168.50.88 255.255.255.0
netsh interface portproxy add v4tov4 listenport=80 listenaddress=0.0.0.0 connectport=80 connectaddress=192.168.50.16
netsh interface portproxy add v4tov4 listenport=3306 listenaddress=0.0.0.0 connectport=3306 connectaddress=192.168.50.16
```
