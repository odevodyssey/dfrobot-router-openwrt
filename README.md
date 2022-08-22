# dfrobot-router-openwrt
OpenWrt SquashFS image for [DFRobot's IoT Router Carrier Board Mini](https://www.dfrobot.com/product-2242.html)

[Video Review](https://youtu.be/o2NTvaRv4Yg)

[DFRobot Carrier Board Wiki](https://wiki.dfrobot.com/Compute_Module_4_IoT_Router_Board_Mini_SKU_DFR0767)

Build based off [OpenWrt 21.02.3](https://github.com/openwrt/openwrt/tree/v21.02.3) (tag v21.02.3)

## Quality of Life Additions

- Added Necessary Packages To Work with DFRobot's IoT Router Carrier Board Mini
  - `kmod-r8169`
  - `kmod-usb-dwc2`
  - `bcm-27xx-userland`
  
  Check manifest file for all included packages, in respective sized folders
  
- Added `br-lan` device to  `/etc/config/network` and referenced in `lan` interface, for ease of setup with WiFi, if desired
- Enabled UART via `/boot/config.txt` file with option `enable_uart=1`
- Secured serial login with password by changing `ttylogin` in `/etc/config/system` to `1`
