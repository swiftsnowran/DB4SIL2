# How to Install a Linux Kernel Which is Compiled

## Install Modules
Use command `make modules_install` to  install modules, and there will be a new folder named "$version$kernel_name" in "/lib/modules".  
**"$version" means the version number of new kernel**   
**"$kernel_name" means the name of the new kernel that was set in configuration step before**

## Install Files Related to Kernel
Use command `make install` to produce "vmlinuz" file and "inittramfs" file and modify config file of grub.   
After execute this command, there will be two new files in "/boot/": inittramfs-$version$kernel_name.img" and "vmlinuz-$version$kernel_name".  
What's more, it will add a new kernel start item in "/boot/grub/grub.cfg".

## Boot
After installation, we can reboot the system directly. 
And then we can use `uname -r` to see the version of the new kernel.