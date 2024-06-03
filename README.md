### Requirements

1. **PC**
2. **Platform Tools**: [Download here](http://developer.android.com/sdk/index.html)
3. **Moto USB Drivers**: [Download here](https://en-us.support.motorola.com/app/usb-drivers)
4. **USB Cable**
5. **Brain**

### Step-by-Step Instructions

#### Step 1: Downloading Platform Tools

1. **Download Platform Tools**:
   - Go to the [Platform Tools download page](http://developer.android.com/sdk/index.html).
   - Download the ZIP file for your operating system.

2. **Install Moto USB Drivers**:
   - Download the drivers from [this link](https://en-us.support.motorola.com/app/usb-drivers).
   - Install the USB drivers on your PC.

3. **Extract the ZIP File**:
   - Extract the contents of the Platform Tools ZIP file to a convenient location on your PC.

4. **Open Platform Tools Folder**:
   - Navigate to the folder where you extracted the Platform Tools.
  
     
![Platform tools](https://github.com/Vinay1a1/G54_custom_rom/blob/main/platform%20tools%20folder.png?raw=true)


5. **Open Command Prompt in Platform Tools Folder**:
   - Click the URL bar
   - Type CMD
   - Press enter

   ![URL](https://github.com/Vinay1a1/G54_custom_rom/blob/main/url.png)
  
   
![CMD](https://github.com/Vinay1a1/G54_custom_rom/blob/main/cmd.png?raw=true)


  ###   **Unlocking Bootloader**
Turn on oem unlocking from settings>developer options
1. **Sign-In Using Google**: Follow the link provided and sign in using your Google account.

2. **Reboot into Bootloader Mode**:
   - Hold the volume down and power buttons simultaneously.
   - Alternatively, use the command: `adb reboot bootloader`.
  
   
![Bootloader](https://github.com/Vinay1a1/G54_custom_rom/blob/main/Bootloader%20mode.jpg?raw=true)


3. **Connect to PC**:
   - Ensure your phone is connected to your PC via USB.

4. **Retrieve Unlock Data**:
   - Open a command prompt/terminal on your PC.
   - Type: `fastboot oem get_unlock_data`.

5. **Copy Unlock Data**:
   - You will see output similar to this:
     ```
     (bootloader) 0A40040192024205#4C4D3556313230
     (bootloader) 30373731363031303332323239#BD00
     (bootloader) 8A672BA4746C2CE02328A2AC0C39F95
     (bootloader) 1A3E5#1F53280002000000000000000
     (bootloader) 0000000
     ```
   - Combine these lines into one continuous string without "bootloader" or spaces. For example:
     ```
     0A40040192024205#4C4D355631323030373731363031303332323239#BD008A672BA4746C2CE02328A2AC0C39F951A3E5#1F532800020000000000000000000000
     ```

6. **Submit Unlock Data**:
   - Paste the combined string on the site you logged in to earlier.
   - Click "Can my device be unlocked?" and agree to the terms.
   - You will receive an unlock key via email.

   
![Moto_website](https://github.com/Vinay1a1/G54_custom_rom/blob/main/Moto%20webiste.png?raw=true)


7. **Unlock Bootloader**:
   - In the command prompt/terminal, type: `fastboot oem unlock <key>`.
   - Replace `<key>` with the unlock code from the email.
   - Confirm the unlock on your phone using the power buttons.

8. **Bootloader Unlocked**:
   - Your bootloader is now unlocked.

    ###    **Flashing Recovery**

1. **Download Recovery**:
   - Obtain the latest recovery image from the appropriate source.

2. **Flash Recovery**:
   - In the command prompt/terminal, type: `fastboot flash vendor_boot recovery.img`.

3. **Reboot to Recovery**:
   - Type: `fastboot reboot recovery`.
  
     
![Recovery](https://github.com/Vinay1a1/G54_custom_rom/blob/main/recovery.png?raw=true)


 ###  **Flashing ROM**

1. **Download ROM**:
   - Get the ROM you want to install. Verify the MD5 checksum to avoid hardbrick.

2. **Apply Update in Recovery**:
   - Boot into recovery mode.
   - Select "Apply update".
  
   
![Apply update](https://github.com/Vinay1a1/G54_custom_rom/blob/main/apply%20update.png?raw=true)


3. **Choose Update Source**:
   - Select either pendrive, SD card, or ADB sideload.
   - If using a PC, type: `adb sideload <rom.zip>`.
   - Replace `<rom.zip>` with the filename or filepath of the ROM.

4. **Flash ROM**:
   - The process will proceed to 47% and then ask if you want to reboot to flash additional packages. Select "Yes" or "No". It doesn't matter what you choose.
  
   
![Flash](https://github.com/Vinay1a1/G54_custom_rom/blob/main/Flash.png?raw=true)


![Reboot_yes_or_no](https://github.com/Vinay1a1/G54_custom_rom/blob/main/Reboot%20yes%20or%20no.jpg?raw=true)


5. **Format Data**:
   - Format data as required by the new ROM.

6. **Reboot to System**:
   - Reboot your phone to the system.

7. **Enjoy New ROM**:
   - Your new ROM is now installed and ready to use.
