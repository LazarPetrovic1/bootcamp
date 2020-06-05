1. Where are the locations of shared libraries stored on your filesystem? Shared libraries are listed in /etc/ld.so.conf 
1. How do you update your apt package sources? apt-get update will update your package sources. 
1. Where can you add default options that apply to all entries in grub? /etc/default/grub is the file used to set grub default options. 
1. What is the main grub configuration file called? grub.cfg is the main configuration file for grub. 
1. Which command would you use to check your grub version? grub-probe --version will tell you the grub version. grub-install --version is also possible but not one of the listed options. 
1. How do you temporarily add a directory to your shared library path? You can temporarily add directories to your shared library path with export LD_LIBRARY_PATH. 
1. How do you update your yum package sources? yum update will update your yum package sources. 
1. Which command will query for the yum package a file belongs to, or was installed by? rpm -qf filename is the correct command. 
1. Which command installs a .deb file? dpkg -i <package name>.deb will attempt to install it. 
1. Where are yum repositories defined? /etc/yum.repos.d contains all the files that define yum repositories. 
