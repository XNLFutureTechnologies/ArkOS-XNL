# Linux Kernel Headers for the R36S / R36H
These are (currently) the original Kernel headers (by christianhaitian) for the <strong>R36S</strong> and <strong>R36H</strong> which are from his official support intended for the RG351MP/RGB10X  

These files are used/needed by the compiler(s) when making or building your own software, drivers and stuff like that on the R36S/R36H consoles.  

If you are using <strong>ANY</strong> other device than the R36S or the R36H then please always use the original (and latest) headers from the original source:
https://github.com/christianhaitian/arkos/tree/main/Headers  

If you're not a developer and are not installing (building!) custom drivers? Just stay away from these files, because you most likely won't ever need them 😉  

## Offline Installation
Obviously it could also be that you would need these files as 'offline installation' when you are still working on getting your wifi/ethernet card working with your R36S/R36H, so that's why you can also use these files with the XNL Package Manager and the Offline Installation Method. Just download all the files in this folder and copy all of them (except the readme.md) to your <strong>OS-TF-CARD</strong> (SDCARD 1!) into the following folder: <strong>/roms/XNLDev/update</strong>  

Then start the XNL Package Manager on your R36S/R36H and goto:  
<strong>->Advanced Packages & Drivers ->Developer Options  Install Kernel Headers</strong>

After <strong>reading the information</strong> and confirming that you do want to install them you can then select option 3:  
<strong>Offline Install (/roms/XNLDev/update)</strong>
  
And the XNL Installation Wizard should do the rest
  
NOTE: The XNLDev needs to be made with the correct capitalization as shown, otherwise you might get issues when running the XNL Package Manager on your system! Most of the time this won't be an issue but just in case it is recommended to make sure the capitalization matches (this depends on the filesystem of your /roms folder and/or how the partition is mounted!)

# What is in KernelCompilers.tar.gz
This archive contains all the <strong>BARE MINIMUM</strong> (.deb) packages needed to make the kernel headers (no worries if you're new to this 😉, this is all automated with my XNL Package Manager). You can install the Kernel Headers but making the headers will require some additional packages (let's call them programs) to be installed, which are not installed by default on your ArkOS/Linux. This is not an mistake or so from the ArkOS developer, but these are just packages which regular users most of the time won't need 😊.  
  
However, if you are going to install the kernel headers, patch them and make them (which is yet again all automated by my XNL Package Manager, no worries), then you will need those 'programs' to be installed to be able to make the kernel scripts.  
  
<strong>NOTE FOR MORE EXPERIANCED LINUX USERS:</strong> Yes, I'm aware that *make scripts* isn't buidling/compiling the kernel headers 😉, I'm just trying to keep it a bit simple here for newcomers to all this😊.  

<strong>Contents of KernelCompilers.tar.gz:</strong>  
```
build-essential_12.8ubuntu1_arm64.deb, libc6-dev_2.30-0ubuntu2.2_arm64.deb, libpython2.7-minimal_2.7.17-1~19.10_arm64.deb, libpython2.7-stdlib_2.7.17-1~19.10_arm64.deb, libpython2-stdlib_2.7.17-1_arm64.deb, libpython-stdlib_2.7.17-1_arm64.deb, libssl-dev_1.1.1c-1ubuntu4.1_arm64.deb, linux-libc-dev_5.3.0-64.58_arm64.deb, python_2.7.17-1_arm64.deb, python2.7_2.7.17-1~19.10_arm64.deb, python2.7-minimal_2.7.17-1~19.10_arm64.deb, python2_2.7.17-1_arm64.deb, python2-minimal_2.7.17-1_arm64.deb, python-minimal_2.7.17-1_arm64.deb  
```

## Offline Installation Warning
While I do understand very well that you sometimes just need to install these packages in offline mode (for example when you are working on (or try to install) a driver for your network card and thus don't have internet access with your device yet). It is however <strong>strongly</strong> recommended to just use the online installers instead where and when possible! Simply because these files are obviously downloaded (and packaged by me) with/for a speciffic device, Linux version and kernel version. Therefor you <strong>can/should not</strong> use them on your device if it doesn't match the following specs:  
Device(s): <strong>R36S</strong> or <strong>R36H</strong>  
ArkOS Version: <strong>12242024</strong> (or later)  
Linux: Ubuntu <strong>19.10</strong>  
Kernel Version: <strong>4.4.189</strong>  
  
In theory my installers/XNL Package Manager should be able to work on other devices which the same specs and OS (like for example the RG351MP/RGB10X) but I do not support any other devices than the R36S and the R36H.  

## Compatibility Check
If you would like to check if your device might be compatible with my installers, packages and my programs/scripts like the XNL Package Manager for example you can check this either manually or by using my <strong>XNL Compatibility Check</strong>  

### XNL Compatibility Check (Automatic Method)
This tool (script) can be downloaded here directly: [XNL Compatibility Check - Direct Link](https://www.teamxnl.com/R36-XCC) or here: [XNL Compatibility Check - GitHub](https://github.com/XNLFutureTechnologies/XNL_R36_Compatibility_Check)   
Just copy this file into the Tools folder on your roms partition, for example: <strong>/roms/Tools</strong> if your on Linux/SSH/FTP etc or <strong>E:\Tools</strong> (replace the E:\ with your roms partition/drive letter of course, which is often called <strong>EASYROMS</strong>)  
  
Then from your console (after reinserting the SD-Card 😉) you go to <strong>Options</strong> (Or <strong>RetroPie</strong> depending on your theme) and there you should be able to find: <strong>XNL Compatibility Check</strong>. Just run that program (script) and you should get a message telling you if your device/installation should be compatible with my tools, packages etc.  
  
NOTE: If you are running it on a device which might be (very) similar to the R36S/R36H, it might also detect it as being compatible, but once again: <strong>I do not offer <u>any</u> support for devices other than the R36S and R36H.</strong>  

### Manual Method
Bascially your device should have files starting with: <strong>rk3326-rg351mp</strong> on it's Boot Partition, it should on the <strong>latest ArkOS</strong>, running on <strong>Ubuntu 19.10</strong>, and have the <strong>4.4.189 Linux kernel</strong> installed.  

You can use the following commands (in the terminal, or over SSH for example):  
<strong>uname -r</strong> should return 4.4.189  
<strong>cat /etc/os-release</strong> should output something like this:  
```
NAME="Ubuntu"
VERSION="19.10 (Eoan Ermine)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 19.10"
VERSION_ID="19.10"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=eoan
UBUNTU_CODENAME=eoan
```

## Online Installation
Online Installation of the kernel headers (and the required patches) is very easy when using the XNL Package Manager. You just start the XNL Package manager and goto:  
<strong>->Advanced Packages & Drivers - ->Developer Options - Install Kernel Headers</strong>

And from there you can choose which installation source you want to use:  
1 XNL Future Technologies GitHub  
2 Official ArkOS GitHub  
3 Offline Install (/roms/XNLDev/update)  
  
Just choose one of the two (online) installation sources and the wizard should do the rest for you. My versions are an exact mirror of the files on the Official ArkOS GitHub and are just here to provide an alternative when you are for example experiencing connection issues and for archive purposes. You can choose either one of them, and when needed (or 'the time comes') I will also make sure that my files are up-to-date with the original kernel headers (although I don't suspect any changes in them anytime soon though).  

The original kernel headers can be found here: https://github.com/christianhaitian/arkos/tree/main/Headers  

And yes, there are more files in that repository than in mine, but that is because my tools etc only focus on the R36S and R36H (which are not officially supported by the ArkOS developer), therefor there are also quite a lot of file we basically don't need.
