# Metasploitable-3-Installation---VMWare

## PART 1 - Commands run to prepare the environment:
1. Before starting this installation, you need to reset your VMWare virtual network settings by going through: Edit - Virtual Network Editor - Change Settings - Restore Defaults
2. Download and Install Vagrant: https://www.vagrantup.com/downloads
3. Download and install Vagrant VMWare utility: https://www.vagrantup.com/docs/provid...
4. Download Packer: https://www.packer.io/downloads
5. Clone repo (download zip file): https://github.com/rapid7/metasploita...
6. Unzip metasploitable3-master.zip to C:\metasploitable3-master
7. Copy packer.exe to C:\metasploitable3-master
8. Use the default vagrantfile that is extracted in C:\metasploitable3-master folder.
9. Run PowerShell as an administrator and change to the folder C:\metasploitable3-master

## PART 2 - Commands run to clean previous installations:
1. vagrant plugin install vagrant-vmware-desktop
2. vagrant box list
  (if any box availabe so remove first)
```
Vagrant box remove rapid7/metasploitable3-ub1404 --provider virtualbox
Vagrant box remove rapid7/metasploitable3-ub1404 --provider vmware_desktop
Vagrant box remove rapid7/metasploitable3-win2k8 --provider virtualbox
Vagrant box remove rapid7/metasploitable3-win2k8 --provider vmware_desktop
```

## PART 3 - Commands run to setup the new installation:
1. vagrant box add rapid7/metasploitable3-ub1404 --provider vmware_desktop
2. vagrant box add rapid7/metasploitable3-win2k8 --provider vmware_desktop
3. vagrant up --provider=vmware_desktop

```
user: vagrant
pass: vagrant
```
