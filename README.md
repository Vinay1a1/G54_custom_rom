
Custom rom in G54
VinayJune 03, 2024
 PC with platform tools and ADB Driver or a secondary mobile with Bugjaegar app. link- https://play.google.com/store/apps/details?id=eu.sisik.hackendebug "NO YOU CANNOT USE WIFI TO CONNECT WITH RECOVERY AND ALSO CANNOT FLASH A69 WITH 5G BASEBAND, SORRY FOR DISAPPOINTMENT " 😞
 
 OTG Cable and compatible USB Cable for Bugjaegar app SD card or Pendrive ( pendrive doesn't work sometimes so use at your own risk, SD card 99.99% times is safe)
 
 Developer Options enabled and USB debugging enabled on both the devices and OEM Unlocking enabled on which you want to flash custom ROM and RECOVERY, MUST
 
 Download Rom file and recovery.img and keep it in SD card in advance. Also keep 'recovery.img' in your PC/secondary device through which you will be using platform tools/Bugjaegar. (These files are available in update group and recovery link can be found in a section below)
 Your bootloader must be unlocked, process is given in a section below.
 
 A 🧠 that functions and has patience.
 
 Some button combos for General Knowledge -Power + volume down long press = Boots into bootloader

Platform tools link- http://developer.android.com/sdk/index.html

Moto usb drivers link- https://en-us.support.motorola.com/app/usb-drivers


Unlocking bootloader

1.  Follow this link here
2. Sign-in using Google
3.  Now reboot your phone into bootloader mode using the instructions above(vol down+ power button or adb reboot bootloader)

Device in bootloader mode
4. Now, connect to pc and type fastboot oem get_unlock_data

5. You will get something like this on your pc screen

(bootloader) 0A40040192024205#4C4D3556313230

 (bootloader) 30373731363031303332323239#BD00

 (bootloader) 8A672BA4746C2CE02328A2AC0C39F95

 (bootloader) 1A3E5#1F53280002000000000000000

 (bootloader) 0000000

6. Paste together the 5 lines of output into one continuous string without "bootloader or info" or white spaces. 

Like- 0A40040192024205#4C4D355631323030373731363031303332323239#BD008A672BA4746C2CE02328A2AC0C39F951A3E5#1F532800020000000000000000000000

7. Copy and paste it on the site you logged in above

8. Click the can my device be unlocked button. Agree the the terms and you will get an unlock key on your mail.

9. Type fastboot oem unlock key

Replace the "key" with the unlock code you received in your email.

10. Click yes in your phone using power buttons.

11.Now, your bootloader is unlocked.


Flashing recovery

 Download the latest recovery from the group.
 Type 

    Fastboot flash vendor_boot recovery.img

 3. Then

    Fastboot reboot recovery

Recovery mode



Flashing Rom

    Download the rom you want from the group. Make sure to verify the MD5 Checksum. Or it may lead to hardbrick.
    Tap apply update in the recovery.
    Choose pendrive/sdcard/adb sideload
    If you are using PC then type 

    Adb sideload rom.zip

Replace rom.zip with the filename or filepath


It will flash till 47% and will ask if you want to reboot to flash additional packages. Select yes if you want to or else press no.

5. Format data.

6. Reboot to system.

7. Enjoy rom.
