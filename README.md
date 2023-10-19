I changed to new laptop, Lenovo G14 GA402RK. This will no longer update in future but i believe just update kext and Opencore it will work in MacOS Sonoma, goodluck!

# Lenovo L340-15IRH Hackintosh Opencore.

*Please check Releases to select EFI according to your version of MacOS.*

## Laptop configuration:
  | **Type** | **Name** | **Note** |
  | --- | --- | --- |
  | CPU | Intel Core i5 9300H | Worked perfectly |
  | Graphics | Intel UHD Graphics 630 | Must disable GTX 1050 |
  | Display | 15.6in LCD FullHD | Undeniably more beautiful than Windows |
  | RAM | 16GB DDR4 | Upgraded from 8GB DDR4 |
  | Wifi| BCM943602CS | Default Wifi Card won't work. |
  | NVME SSD| Samsung SSD 970 EVO Plus 250GB | No default NVME SSD default |
  | SATA HDD | ST1000LM024 1TB | Used for saving 3 Operating Systems data |
  | USB | 2 USB 3.1 + 1 USB 3.1 Type C | Worked perfectly |
  | Trackpad | Synaptics | Worked well |
  | Audio | Realtek ALC 257 | Worked fine with layout 18 |
  | OS version| 13.1 | The latest version up to now |
  


## Working:

  **CPU** (get all kernels and threads, the lowest clock speed is lowered to 0.8Ghz).
  
  **iGPU** (works fine with acceleration; I changed the ID to Iris Plus 655 for fun; increased the VRAM to 4095 MB; and renamed it to RTX 3090 to make it look stronger :)) ).
  
  **Screen** (Brightness, NightShift worked fine, and is undeniably more beautiful than Windows).
  
  **Trackpad/Keyboard** (Force-click and gesture works fine)
  (Controls for volume (Fn + F1/F2/F3), Brightness (Fn + K/P), Control media (Play/Pause/Next) and Hide mouse(Fn + Esc) are all included).
  
  **Wi-Fi** (It worked perfectly, received both 2.4GHz and 5GHz, and supports for 802.11 a/b/g/n/ac).
  
  **Bluetooth** (works flawlessly).
  
  **Ethernet, USB tethering** (worked well).
  
  **Audio** (worked fine, layout 18).
  
  **Battery** (Can use 2 to 3 hours depending on the task, with a weak battery (3342 mAh) ).
  
  **Disk** (Samsung nvme 970 should turn off TRIM to avoid hard drive error every time it boots)
  
  **SecureBoot** (work with 1s delay using Super UEFIinSecureBoot Disk)
  
  **Camera, USB, iSevice(iMess, Facetime, Airplay, Sidecar, Handoff, AirDrop, Universal Clipboard), etc.**
  
## Not tested:

  Buy Macbook, actually afford a Macbook ( ͡° ͜ʖ ͡°)

## Not working:

  **dGPU** (it can work, but it will crash and cause the iGPU (which doesn't have a MUX switch) to fail).
  
  **HDMI** (It's connected to the GTX 1050, which was disabled in DSDT; if possible, I'll fix it).
  
  **Led status of the NumLock** (Not sure why, but please contact me if you know fix it).
  
  **~~Secure boot~~** Now you can use it through new update
  
  **PrtScr key** not work, Fn + F5 and PrtScr keys will make your mouse freeze for a few seconds.
  
## Note:
  
  ***Wireless:***
  Original WiFi card will never work, it's basically impossible. Recommend buying a Realmac card
  
  ***dGPU:***
  It may actually work, but MacOS doesn't natively support it and never will in the future(I wish it had support for MUX switching, or at least there was a way). If you want to see it work with dGPU 700Mb of VRAM and iGPU 7Mb of VRAM and "enjoy" the lag, try this:
  
  [OpenCore Legacy Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher)
     
  ***Trackpad:***
  If there are a few reboots or wakes, the trackpad will not work. Usually after using it for a while, it won't have any error. So if you encounter it, don't worry, just close your laptop, make coffee, and go back. It should be fixed, it's magic.
  
  ***HiDPI:***
    You can use HiDPI to see everything more clearly. There are two commands below:
  ```
      sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool true
  ```
    
  ```
      bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
  ```
  
   If you use HiDPI, I recommend you to use anti-aliasing to reduce font blur, run the following 2 commands and reboot
    
    
  ```
  defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO
  ```
  
  ```
  defaults -currentHost write -globalDomain AppleFontSmoothing -int 3
  ```
  
  ***Hibernation:***
  You should use Hibernation mode instead of Sleep mode since it saves more battery. You just need to run the following command, the rest is fixed:
   ```
      sudo pmset hibernatemode 25
  ```
  ***SecureBoot:***
  Now you can use it through new update, supported by Super UEFIinSecureBoot Disk. First you should open secureboot in BIOS, boot as usual, if it asks for  signature, press **OK** and choose **Enroll cert from file** menu option. Select Phuchau.cer on **EFI/BOOT** and confirm certificate enrolling, at the end you select **Yes** and then **Reboot**.
  
  If you update OpenCore to a newer version and you see I don't update, you can update OpenCore and still keep secureboot by the following: the new OpenCore **BOOTX64.EFI** file you rename it to **grubx64_real.efi** (overwrite the old file), then you rename the backup file  **BOOTX64.EFI.SB** and rename it back to **BOOTX64.EFI** (overwrite the old file), done.

  
## Contact me:

  [Facebook](https://www.facebook.com/thaihoangphuchau)
  
  [Gmail](MAILTO:phuchau.developer@gmail.com)
