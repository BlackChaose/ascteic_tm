### Install WSL ###

* [link](https://pureinfotech.com/install-windows-subsystem-linux-2-windows-10/)

* Enable Windows Subsystem for Linux 1 (in Windows features)
* Enable Virtual Machine Platform (in PS run: ```Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform```)
* Restart PC
* Download [update](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
* install update
* Set default WSL2 version (in PS run: ```wsl --set-version Ubuntu 2```)
* check version WSL in PS run ```wsl --list --verbose```
