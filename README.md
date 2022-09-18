# L340_15IRH_Hackintosh
Lenovo L340-15IRH Hackintosh Opencore

*Please check Releases to select EFI according to your version of MacOS.*


**Laptop configuration:**
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
| Audio | Realtek ALC 257 | works fine layout 18 |
| OS version| 13.0 Beta (22A5342f) | Works fine |
  


**Working:**

  CPU (get all kernels and threads)
  
  iGPU (with acceleration, change id to Iris plus 655, increase VRAM to 4095 MB and rename to RTX 3090 (for fun and look it strong))
  
  Screen Brightness, NightShift (works fine, more beautiful than windows is undeniable)
  
  Trackpad/Keyboard (Force click and gesture works fine)
  (includes volume function (Fn + F1/F2/F3 key) Brightness (Fn + K/P) and Control media (Play/Pause/Next), Hide mouse(Fn + Esc))
  
  Wi-Fi (works fine(of course), get both 2.4GHz and 5GHz, 802.11 a/b/g/n/ac)
  
  Ethernet, USB tethering (works fine)
  
  Audio (works fine)
  
  Bluetooth (works fine)
  
  Battery level (works fine)
  
  iSevice, iMess, Facetime, Airplay, Sidecar, Handoff, AirDrop, Universal Clipboard,...
  
  Camera, USB, etc...
  
   ***Optimize***
    You can open HIDPI to see everything more clearly, there are 2 ways, first way with the command below:
  ```
      sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool true
  ```
    or(recommended)
  ```
      bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
  ```
  
  ***Hibernation***
  You should use hibernation instead of sleep because it will save more battery, you just need to run the following command, the rest is fixed
   ```
      sudo pmset hibernatemode 25
  ```
  
**Not tested:**

  Nope :)))

**Not working:**

  dGPU(can make it work but will crash and cause iGPU to not work (due not MUX switch))
  
  HDMI(You can't use HDMI because HDMI is connected with GTX 1050 and that was disabled in DSDT, i will fix it if possible)
  
  NumLock led on/off(I don't understand why, you know please contact me so I can fix it)
  
  Key PrtSC not work, Fn + F5 and PrtSc will make your mouse freeze for a few seconds
  
  **Contact me:**
  Facebook: https://www.facebook.com/phuchau.developer@gmail.com
  Gmail: phuchau.developer@gmail.com
