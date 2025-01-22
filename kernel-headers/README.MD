# Linux Kernel Headers for the R36S / R36H
These are (currently) the original Kernel headers (by christianhaitian) for the <strong>R36S</strong> and <strong>R36H</strong> which are from his official support intended for the RG351MP/RGB10X

These files are used/needed by the compiler(s) when making or building your own software, drivers and stuff like that on the R36S/R36H consoles.

If you are using <strong>ANY</strong> other device than the R36S or the R36H then please always use the original (and latest) headers from the original source:
https://github.com/christianhaitian/arkos/tree/main/Headers

If you're not a developer and are not installing (building!) custom drivers? Just stay away from these files, because you most likely won't ever need them 😉😂

## Offline Installation
Obviously it could also be that you would need these files as 'offline installation' when you are still working on getting your wifi/ethernet card working with your R36S/R36H, so that's why you can also use these files with the XNL Package Manager and the Offline Installation Method. Just download all the files in this folder and copy all of them (except the readme.md) to your <strong>OS-TF-CARD</strong> (SDCARD 1!) into the following folder:
/roms/XNLDev/update

Then start the XNL Package Manager on your R36S/R36H and goto:
<strong>->Advanced Packages & Drivers ->Developer Options  Install Kernel Headers</strong>

After <strong>reading the information</strong> and confirming that you do want to install them you can then select option 4:
<strong>Offline Install (/romd/XNLDev/update)</strong>

And the XNL Installation Wizard should do the rest

NOTE: The XNLDev needs to be made with the correct capitalization as shown, otherwise you might get issues when running the XNL Package Manager on your system! Most of the time this won't be an issue but just in case it is recommended to make sure the capitalization matches (this depends on the filesystem of your /roms folder and/or how the partition is mounted!)

## Online Installation
Online Installation of the kernel headers (and the required patches) is very easy when using the XNL Package Manager. You just start the XNL Package manager and goto:
<strong>->Advanced Packages & Drivers ->Developer Options  Install Kernel Headers</strong>

And from there you can choose which installation source you want to use:
1 XNL Future Technologies GitHub
2 Official ArkOS GitHub
3 Offline Install (/roms/XNLDev/update)

Just choose one of the two (online) installation sources and the wizard should do the rest for you. My versions are an exact mirror of the files on the Official ArkOS GitHub and are just here to provide an alternative when you are for example experiencing connection issues and for archive purposes. You can choose either one of them, and when needed (or 'the time comes') I will also make sure that my files are up-to-date with the original kernel headers (although I don't suspect any changes in them anytime soon though) 
The original kernel headers can be found here: https://github.com/christianhaitian/arkos/tree/main/Headers

And yes, there are more files in that repository than in mine, but that is because my tools etc only focus on the R36S and R36H (which are not officially supported by the ArkOS developer), therefor there are also quite a lot of file we basically don't need.

