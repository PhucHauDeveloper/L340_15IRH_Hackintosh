# L340_15IRH_Hackintosh
Lenovo L340-15IRH Hackintosh Opencore.

*Please check Releases to select EFI according to your version of MacOS.*


## Laptop configuration:
  | Type | Name | Note |
  | --- | --- | --- |
  | CPU | Intel Core i5 9300H | Works fine |
  | Graphics | Intel UHD Graphics 630 | Disabled GTX 1050 |
  | Display | 15.6in FullHD | More beautiful than windows is undeniable |
  | RAM | 16GB DDR4 | Upgraded from 8GB DDR4 |
  | Wifi| BCM943602CS | Default Wifi never work. |
  | NVME SSD| Samsung SSD 970 EVO Plus 250GB | No SSD default|
  | SATA Disk | ST1000LM024 1TB | I save the data of 3 operating systems on this hard drive |
  | USB | 2 USB 3.1 + 1 USB 3.1 Type C | Works fine |
  | Trackpad | Synaptics | Works fine |
  | Audio | Realtek ALC 257 | Works fine layout 18 |
  | OS version| 13.0 Beta (22A5342f) | Works fine |
  


## Working:

  CPU (get all kernels and threads).
  
  iGPU (works fine with acceleration; for fun and to appear powerful, I changed the ID to Iris Plus 655; increased the VRAM to 4095 MB; and renamed it to RTX 3090).
  
  Screen Brightness, NightShift (works fine, and is undeniably more beautiful than Windows).
  
  Trackpad/Keyboard (Force click and gesture works fine)
  (Controls for volume (Fn + F1/F2/F3), Brightness (Fn + K/P), Control media (Play/Pause/Next) and Hide mouse(Fn + Esc) are all included).
  
  Wi-Fi (It works perfectly (of course), receives both 2.4GHz and 5GHz, and supports 802.11 a/b/g/n/ac).
  
  Bluetooth (works flawlessly, of course).
  
  Ethernet, USB tethering (works fine)
  
  Audio (works fine, layout 18)
  
  Battery level (works fine)
  
  Camera, USB, iSevice(iMess, Facetime, Airplay, Sidecar, Handoff, AirDrop, Universal Clipboard), etc.
  
## Not tested:

  Nope :)))

## Not working:

  dGPU (can make it work, but it will crash and cause the iGPU (which doesn't have a MUX switch) to fail).
  
  HDMI (You can't use HDMI because it's connected to the GTX 1050, which was disabled in DSDT; if possible, I'll fix it).
  
  Led status of the NumLock (I'm not sure why, but please contact me so I can fix it).
  
  PrtSC key not work, Fn + F5 and PrtSc keys will make your mouse freeze for a few seconds.
  
## Note:
  
  *Wireless:*
  Don't try to make the original WiFi card work; it's impossible. Buy a Realmac card for the best experience
  
  *dGPU:*
  It may actually work, but MacOS doesn't natively support it and never will in the future(I wish it had support for MUX switching, or at least there was a way). If you want to see it work with dGPU 700Mb of VRAM and iGPU 7Mb of VRAM and "enjoy" the lag, try this:
  
  [OpenCore Legacy Patcher](https://github.com/dortania/OpenCore-Legacy-Patcher)
     
  *Trackpad:*
  If there are a few reboots or wakes, then the trackpad will not work. Usually, after using it for a while, it will not error, so if you encounter it, don't worry. Just close the laptop, make a cup of coffee, and go back to it. It's fixed, it's magic.
  
  *HiDPI*
    You can use HiDPI to see everything more clearly. There are 2 ways: first with the command below:
  ```
      sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool true
  ```
    or(recommended)
  ```
      bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
  ```
  
  *Hibernation*
  You should use hibernation instead of sleep because it will save more battery life. You just need to run the following command. The rest is fixed:
   ```
      sudo pmset hibernatemode 25
  ```
  
## Contact me:

  [Facebook](https://www.facebook.com/phuchau.developer@gmail.com)
  
  [Gmail](phuchau.developer@gmail.com)
