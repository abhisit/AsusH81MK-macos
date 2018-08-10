# Asus H81M-K macOS Install Resources

This project created for working macOS  Clover Configuration. Worked with this board and Core i3/i5/i7 CPUs with HD4400/4600 graphics. Builds will be updated at future.

## Step-by-step guide

* Download macOS via Mac App Store

* Download or clone this repo

* Download latest BIOS (version 3602 at last moment) [here](https://www.asus.com/Motherboards/H81MK/HelpDesk_BIOS/) and flash via ASUS EZ Flash - guide [here](https://www.asus.com/support/FAQ/1012154/)

* Reset BIOS to default and check this settings:

```
- CSM(Compability Support Module): Disabled
- iGPU Memory: 96MB
- CPU MSR Lock: Disabled
- Sata Configuration: AHCI
- USB Mode: Smart Auto
- Fast Boot: Disabled
- Secure Boot: Other OS
- Intel RapidStart/SmartConnect: Disabled
```

* Prepare macOS USB Installation Drive - guide [here](https://www.ifixit.com/Guide/Create+a+bootable+USB+drive/66371)

* Download latest Clover Bootloader [here](https://sourceforge.net/projects/cloverefiboot/files/latest/download), install it on USB Insallation Drive for UEFI Boot via few additional drivers: AppleImageCodec,AppleKeyAgregator,AppleUITheme,DataHubDxe,FirmwareVolume,FSInject,SMCHelper,VBoxHfs,OsxAptioFix3Drv.
`Install Apfs Driver loader from Clover Installer on USB Drive ONLY if you have SSD Drives`

* Copy DSDT.aml from ACPI folder and copy to /EFI/CLOVER/ACPI/patched on USB Drive

* Copy config.plist to /EFI/CLOVER

* Copy kexts of "kexts/other" folder and copy to /EFI/CLOVER/kexts/10.13 on USB Drive

* Boot and install macOS from USB Drive - guide [here](https://hackintosher.com/guides/macos-high-sierra-hackintosh-install-clover-walkthrough/)

* After succesfully (i hope) install Clover to macOS drive and copy files from USB Drive

* Open your config.plist from EFI/CLOVER [here](http://cloudclovereditor.altervista.org/cce/index.php) and generate SMBIOS (iMac 14,1) at new serial number, or use this [guide](https://www.tonymacx86.com/threads/guide-how-to-configure-your-systems-smbios-correctly.198155/)

* ???

* Profit!!!

### Notes

* Please check graphics freq (not tested), normally - 0.2 to 1.15 Ghz (use Intel Power Gadget)

* Older versions of macOS may be needed additional patches/fixes, but it's may be working too.

### Changelog

#### 1.0 (16 May 2018) 
- Initial release for macOS High Sierra 10.13.4 

#### 1.1 (6 Aug 2018) 
- Repo updated to macOS High Sierra 10.13.6

### Credits

 - [@RehabMan](https://github.com/RehabMan): patches, kexts and amazing job 
 - [@Ty3uK](https://github.com/Ty3uK): for idea and link to [Hackintosh Installer University](https://github.com/huangyz0918/Hackintosh-Installer-University)
 - [Hackintosh Installer University](https://github.com/huangyz0918/Hackintosh-Installer-University): it's amazing project for Hackintosh Community
 - [@vit9696](https://github.com/vit9696) - The chief Russian developer of decisions for Hackintosh

Credits by [@Slbomber](https://github.com/Slbomber), 2018
