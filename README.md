# ASUS-ZenBook-Pro-Duo-15-OLED-UX582-Hackintosh
Hackintosh installation guide for ASUS ZenBook Pro Duo 15 OLED UX582

<p>
<img src="https://raw.githubusercontent.com/shiecldk/ASUS-ZenBook-Pro-Duo-15-OLED-UX582-Hackintosh/main/images/UX582.png" alt="UX582" class="center"></p>

## License
This repo is protected by GNU GPL license. Any commercial use of this project without authorization is strictively prohabited. Please refer to this repository when making any distribution.


## External Guide
<p>
<a href="https://www.insanelymac.com/forum/topic/349049-guide-asus-zenbook-pro-duo-15-oled-ux582/">macOS Installation Guide on InsanelyMac</a><br>
<a href="https://www.tonymacx86.com/threads/guide-asus-zenbook-pro-duo-15-oled-ux582-opencore.315661/">macOS Big Sur Installation Guide on Tonymacx86</a></p>


## Spec
| Component | Brand |
| ----------- | ----------- |
| CPU | Intel Core i9-10980HK (varient: Intel Core i7-10870H) |
| iGPU | Intel UHD Graphics 630 |
| dGPU | Nvidia RTX 3070 (won't work; disabled to save battery; could be enabled with <a href="https://github.com/acidanthera/UEFIGraphicsFB"> UEFIGraphicsFB.kext </a> for HDMI port without graphics acceleration) |
| Audio | Realtek ALC294 |
| Ram | 32GB DDR4L 2933 MHz (varient: 16GB DDR4L 2933 MHz) |
| Wifi + Bluetooth | Intel AX201 Wifi 6, Bluetooth 5.0 |
| Storage | Samsung PM981A 1TB M.2 SSD (replacement needed) |
| Camera | Windows Hello HD Camera with IR |
| Trackpad | ELAN1406, 04F3:3101 |
| Display | 15.6" (3840x2160) OLED; 14" (3840x1100) IPS ScreenPad Plus |
| Touch Screen| ELAN9008, \_SB.PCI0.I2C1.TPL0, 04F3:2C56; ELAN9009, \_SB.PCI0.I2C1.TPL1, 04F3:2C23 |
| Stylus | ASUS Pen SA201H  |
| Ports | 1x USB 3.2 Gen 2 Type-A; 2x Thunderbolt 3; 1x HDMI 2.1; 1x 3.5mm Combo Audio Jack; 1x DC-in |
| Battery | 92Wh 15.48v 5810mAh |


## ToDo List
- [ ] Brightness auto adjustment with ambient sensor
- [ ] Some other FN keys (FN+F10, fan control, switch main/secondary monitors, and disable secondary monitor)
- [ ] Trackpad GPIO mode
- [ ] Numpad
- [ ] Thunderbolt 3 for eGPU (need more SSDT and DROM patches)


## Current progress

### What's working
- [x] macOS Monterey
- [x] macOS Big Sur
- [x] macOS Catalina
- [x] Intel UHD Graphics 630
- [x] Intel WiFi 6 (speed could be slow on some very few routers)
- [x] Intel bluetooth
- [x] Internal stereo speaker
- [x] Internal microphone
- [x] Combo audio jack
- [x] Camera
- [x] Battery indication
- [x] CPU SpeedStep
- [x] Main touchscreen
- [x] Secondary ScreenPad Plus
- [x] Brightness control (software brightness control workaround with <a href="https://github.com/alin23/Lunar/issues/398">Lunar</a>)
- [x] Stylus pen (works on both screens without sense of pressure)
- [x] Keyboard
- [x] Trackpad
- [x] FN keys for volume, brightness, keyboard backlight, and enable/disable trackpad
- [x] USB 3.2 Gen2 Type-A
- [x] USB 3 Type-C
- [x] USB 3 Type-C to DP/HDMI (only one port works due to macOS restriction)
- [x] Thunderbolt 3 (only non-eGPU devices work for now)
- [x] Power adaptor
- [x] Sleep/wake
- [x] iCloud
- [x] Continuity

### What's not working for now
- [ ] Nvidia RTX 3070 (won't work due to no driver in macOS)
- [ ] HDMI port (routed to Nvidia RTX 3070; same as above)
- [ ] Native brightness control with macOS CoreDisplay (need to port driver from Linux for display brightness control; check <a href="https://github.com/s-light/ASUS-ZenBook-Pro-Duo-UX581GV/tree/master/screen_brightness">s-light/ASUS-ZenBook-Pro-Duo-UX581GV</a>)
- [ ] Ambient light sensor (same as above)
- [ ] Thunderbolt eGPU (WIP; need to work with DROM and SSDT)
- [ ] Numpad (need to port driver from Linux; check <a href="https://github.com/mohamed-badaoui/asus-touchpad-numpad-driver">mohamed-badaoui/asus-touchpad-numpad-driver</a>)
- [ ] Some other FN keys (WIP; check <a href="https://github.com/hieplpvip/AsusSMC">hieplpvip/AsusSMC</a>)

## HiDPI on ScreenPad Plus in macOS Ventura
To enable HiDPI on the ScreenPad Plus in macOS Ventura:

1. Use [one-key-hidpi](https://github.com/xzhih/one-key-hidpi) to enable HiDPI.
2. Use either [RDM](https://github.com/avibrazil/RDM) or SwitchResX to switch to HiDPI resolutions.

Note: In macOS Ventura, only 2560x733 and 2048x587 HiDPI resolutions are currently working on the ScreenPad Plus. The previously functional 1920x550 (HiDPI) resolution is no longer available. The native resolution remains 3820x1100.


## Support this Project
If you like this guide, please consider donating me through PayPal or crypto. Developement of this hackintosh consumes a lof of time. You can contribute to this project by buying me a cup of coffee to keep this repo up-to-date.

<p>
<a href="https://www.paypal.com/donate/?hosted_button_id=YK65DJNB4UK2L">
         <img alt="Paypal" src="https://raw.githubusercontent.com/shiecldk/ASUS-ZenBook-Pro-Duo-15-OLED-UX582-Hackintosh/main/images/PayPal.png"
          height="140"></a><br>
<a href="https://www.paypal.com/donate/?hosted_button_id=YK65DJNB4UK2L">Donate with PayPal</a></p>

<p>BTC Address: 1jUMQVzq9e64erkytLYuD1LTt7nMkAFXs<br>
ETH Address: 0x09bbd23a1fe39cc70aba2232dcd9d1aa64a3fb2d<br>
SOL Address: HPrnqBfDArW3xcQqGZZ1Y51QSbJMFtoVtmtnufySqynD<br>
ADA Address: Ae2tdPwUPEZMsWbd5xpjBD9rvurtkdPq4p7mPZMsmbcbTR1wAhsYkGVMGza</p>


## Credits
- Apple for macOS
- acidanthera for OpenCore and most kexts
- atrslb for many things I couldn't achieve
- gvkt for ScreenPad VoodooI2C fix
- Qonfused for developing and maintaining the project
- [wern-apfel (as he complained here)](https://github.com/hieplpvip/AsusSMC/issues/108#issuecomment-1422929407) for some SSDTs for Qonfused's work
- Rehabman
- Many others
