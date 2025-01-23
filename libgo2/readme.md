# libgo2 Development Headers
Minimal developmenent headers for the R36S/R36H from: https://github.com/christianhaitian/libgo2
Used for the ArkOS / ArkOS-XNL Development Mode.   
  
These can be used if you manually want to install/copy them onto your R36S/R36H, installation is basically quite simple,  
The files in this folder should go in the exact same folders on your R36S/R36H as they are presented here so basically:  
<strong>/usr/include/go2</strong>  
  
NOTE: This needs to be in your Linux partition! NOT on your (windows accesible) partition(s)! and thus for example NOT on your roms partition! These should for example be transfered with an FTP program like FileZilla or using SSH.
  
For most user I would personally recommend to just use the XNL Package Manager to install them. You can either install them using one of the online installation methods, or even use the offline installer by downloading the <strong>librga-libgo2.tar.gz</strong> file from the <strong>XNL Installation Manager Packages</strong> directory in the root of this (ArkOS-XNL) repository and then copying it to the folder <strong>/roms/XNLDev/update</strong> folder on the <strong>TF-OS-CARD</strong> (SDCARD 1!).  

You can then select the <strong>Offline Install (/roms/XNLDev/update)</strong> source option from the XNL Package Manager which you can find in:  
<strong>->Advanced Packages & Drivers - ->Developer Options - Install librga & libgo2 Headers</strong>  
  
When using the XNL Package Manager it will install both development headers at once (librga and libgo2) for the R36S/R36H  


My package for the libgo2 however only contains a few files (all that are needed for the ON the R36S/R36H by default), you can find more information and additional files here on the full repository from the developer of ArkOS: https://github.com/christianhaitian/libgo2
