# XNL Installation Manager Packages
These are installation packages which can be used by the <strong>XNL Package Manager</strong> on your <strong>R36S/R36H</strong> to install additional utils, programs, drivers and more. When using the XNL Package Manager you can for some packages choose an installation source, and when you are given the option to use the XNL Future Technologies GitHub, then chances are that package package is dowloaded from this directory (except for the <strong>Kernel Headers</strong>, those can be found in the root of this repository).  

Some tools, add-ons etc are already included in the default <strong>XNL R36 Tool Kit</strong>, while others can be installed as additional options. This will also give me the option to let users customize their install more to what they want to install and what not. Some tools/programs/tools might be a bit more complex and therefor will remain part of the main XNL R36 Toolkit.  

Most of the packages in this directory can also be used as Offline Installer when needed. You can then download the desired <strong>.tar.gz</strong> file(s) and then select the package/installation that uses those files. For example: When you want to install the librga and libgo2 development headers in 'offline mode', you can download the <strong>librga-libgo2.tar.gz</strong> file, then place it (on your OS-TF-CARD / SDCARD 1!) in the folder <strong>/roms/XNLDev/update</strong>  

Then on your R36S/R36H you start the XNL Package Manager and goto <strong></strong>->Advanced Packages & Drivers - ->Developer Options - Install librga & libgo2 Headers</strong>, then after <strong>reading the information presented</strong> you can click on Yes and then select <strong>Offline Install (/roms/XNLDev/update)</strong>

## Can I use these packages to (fully) manually install these tools, drivers, applications etc?
No you can't. Well you could, IF you would know the exact process required for each package. Some of these packages (most actually) require additional steps, command, system configuration etc to install them properly. These archives (the .tar.gz files) however DO NOT contain any install scripts or whatever. They for example only contain binaries, .deb packages, headers etc. The XNL R36 Package Manager can (and should) be used to properly install, update and uninstall these packages. The XNL R36 Package Manager is designed to make installation of these package super easy with a user friendly user interface and full automation of the process.  
  
<strong>Where can I find the XNL R36 Package Manager?</strong>  
Currently it's still in development, but like mentioned on the main page I do need (quite) some files to be online already (like these packages for example) to be sure that it works as flawless as possible over a real internet connection (and not just a locally hosted repository for example). Once the XNL R36 Package Manager is release you will be able to find it both on my website and on my GitHub (links will follow when it is released)  
  
## Can I use these packages and/or your scripts/tools/software for other devices than the R36S/R36H?
You could <strong>probably</strong> use my tools/software etc on any other device running on the same ArkOS version which is used for the <strong>R36S/R36H</strong> (which is the <strong>RG351MP/RGB10X</strong> version). It should in <strong>theory</strong> be possible but I do not offer support and will not add support for any other device(s) than listed in my projects/software. Simply because these devices are not my main project, not 'the thing' I spend all day on (retro gaming etc), and because I only make (and test) tools/scripts/software etc on devices on which I can actually physically test it my self (and thus own).  

You could try running my tools/software and scripts on other devices than the R36S/R36H (<strong>at your own risk of course</strong>), It is however important that the specs match the R36S/R36H:  
CPU: <strong>RK3326</strong>  
GPU: <strong>Mali-G31 MP2</strong>  
RAM: <strong>1GB</strong>  
Architecture: <strong>32bit & 64bit (aarch64)</strong>  
Screen Resolution: <strong>640x480</strong>  
Linux Kernel: <strong>4.4.189</strong> (<strong>IMPORTANT!</strong>)  
Linux Distro: <strong>Ubuntu 19.10 (Eoan)</strong>  

Personally I suspect that my tools/scripts/programs will work on much more devices than only the R36S/R36H and the RG351MP/RGB10X range, but that's all up to you to try for yourself. If so you can always let me know and maybe I might eventually publish a list of devices on which my tools also work. Something like a *"Confirmed by the community to work on the following (nonsupported) devices:"* list  

