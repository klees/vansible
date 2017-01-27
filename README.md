
# VANSIBE
**Vansible automaticly installs a development environment with multiple virtualbox machines.**

## Usage
### Software Requirements
* Linux or MacOs
* [Vagrant]
* [Ansible]
* [VirtualBox]
* [git]

### Installation
```
$ cd DESTINATION_FOLDER
$ git clone https://github.com/daniwe4/vansible.git
$ cd Vansible
```
### Configuration
All configuration tasks can be done in one file. Open the file "goup_vars/all/config.yml".
Each section is well commentet. Fell free to update each section for your own needs.

### First Start
The first start has to be with root priviliges. It will create a symlink, so from now on you only need the command "vag".
```
$ sudo ./vag.py up
```
Dependent on how much machines and how much roles you defined in the config, this stepp can take a few minutes.

### Following Starts
Start or Install machines:
```
$ vag up [machinename]
```
Stop machines:
````
$ vag stop [machinename]
````
Update machines:
````
$ vag provision [machinename]
````
Destroy machines:
````
$ vag destroy [machinename]
````

### Access To The Machine

To access to the console of the virtual machine you can use the following command:
````
$ vag ssh [machinename]
````
To access the folder structure of the virtual machines i suggest to use sshfs.
````
$ sshfs root@<vm_ip_address>:/home/ <mount_dir_on_host>
````

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [Vagrant]: <https://www.vagrantup.com/>
   [Ansible]: <https://www.ansible.com/>
   [VirtualBox]: <https://www.virtualbox.org/>
   [git]: <https://git-scm.com/>