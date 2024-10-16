## To check if you have an empty slot
1. Connect device in fastboot
2. Open command prompt
3. Type: fastboot getvar all
4. Hit enter
5. Check the lines with slot_unbootable
6. If it says "yes" then you need to fix it
7. Example-
   
      `(bootloader) slot-successful:_a: yes`
   
      `(bootloader) slot-successful:_b: no`
   
      `(bootloader) slot-unbootable:_a: no`
   
      `(bootloader) slot-unbootable:_b: yes`

   
## Requirements 
1. Download tiny fastboot script from lolinet- https://mirrors.lolinet.com/software/windows/TinyFastbootScript/
2. Your device firmware(one version older than the one you wish to be on) from- https://mirrors.lolinet.com/firmware/lenomola/
3. Brain
4. Eyes


## To fix it, follow the steps

## Steps
1. Extract both TFS and firmware in the same folder
 ![Image showing both in same folder](https://github.com/Vinay1a1/G54_custom_rom/blob/main/Screenshot%20(12).png)
2. Run flash.bat
3. Use the default bootloader version(1st option)
4. Press 5 to flash full firmware and factory reset
 ![Image showing TFS screen](https://github.com/Vinay1a1/G54_custom_rom/blob/main/TFS.png)
5. Wait
6. Boot your phone in system once flashing is completed
7. Go to updates in settings
8. Do an OTA and reboot


Now your slots are fixed. You can flash custom rom without any issues.

Credits- Me, Lolinet guys and our hardworking devs.
