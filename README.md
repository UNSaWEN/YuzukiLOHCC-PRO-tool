# YuzukiLOHCC PRO
Yuzuki **L**oop **O**ut **H**DMI **C**apture **C**ard PRO

**CERN Open Hardware Licence Version 2 - Permissive**

Low cost USB3.2Gen1 HDMI-USB Video Acquisition With Loop Out (Loop Out HDMI Capture Card)

![main](Bitmap/LOHCC.jpg)
## fork update:
Add windows flash tool and Firmware.  
using ref(Chinese):https://post.smzdm.com/p/a0qp94n9/

>backup
>1. using option MS2130/31
>2. choose Flash
>3. Connect
>4. Read
>5. Save To Bin

>flash
>1. Open File
>2. Connect
>3. Download
>4. plugout and reconnect

## About

Ultra low cost Loop Out HDMI-USB Video Acquisition (HDMI Capture Card) based on MS2130 and MS9332 + MS8003

MS2130 is a USB 3.2 Gen 1 high-definition video and audio acquisition chip, which is internally integrated with USB 3.2 Gen 1 Device controller, data transceiver module, and audio and video processing module. The MS2130 can transmit the audio and video signals input by HDMI to a PC, smartphone, or tablet for preview or collection through the USB 3.2 Gen 1 interface. The MS2130 output supports YUV422 and MJPEG modes, and is compatible with Windows, Linux, Android and Mac OS systems. Support OBS Studio, Camera, and FFmpeg.

- Support HDMI 4Kx2K@30Hz and HDMI 2.0, YCbCr420 4Kx2K@60Hz Loop Out
- Support 10/12/16 bit Deep Color for Loop Out
- Adaptive input equalization for Loop Out
- Integrated pre-programmed HDCP keys for Loop Out
- Embedded EDID RAM for Loop Out
- USB Type-C USB3.2 Gen 1 interface
- Full height HDMI x 2
- Compatible with DVI 1.0
- Support YUV&JPEG output
- Compatible with UVC 1.0, UAC 1.0
- Support audio capture
- Support video capture
- Maximum video input 3840x2160@30
- The highest output resolution is 4096x2160@15
- Support 1920x1080@60
- Support Windows 7 Above, macOS 10 and later, Linux, Android and so on
- Standed UVC 1.0, Support OBS Studio, Camera, FFmpeg and so on.

## Basic 

![main](Bitmap/LOHCC_Basic.png)

## Order a PCB
Here I suggest using [JLCPCB](https://jlcpcb.com/) to make PCB (my template is also made by JLCPCB). Please note that the **impedance needs to be 3313**, and the **PCB thickness needs to be 0.8mm to install the clamp-style TypeC connector**

![image](https://user-images.githubusercontent.com/12003087/195976170-9df155ec-adb7-4d5e-a0ef-b54f514ab2f4.png)


### Supported USB output resolution table

![res](Bitmap/reslist.png)

## Flash Firmware

### USB Flash

Using [ms-tools](https://github.com/BertoldVdb/ms-tools) from @BertoldVdb
```
./cli --log-level=7 write-file --verify FLASH 0 YuzukiLOHCCPro.bin
```

### SPI Programmer

Use an SPI NOR flasher to flash the firmware to the NOR Flash before soldering.

(Only one of `U4` and `U8` needs to be mounted, adding two SPI NOR pads are drawn to be compatible with different types of materials)

![eeprom](Bitmap/EEPROM.png)

**Unfortunately, I couldn't find a public version of the MS8003 code, but it's not expensive to buy a pre-programmed set**

## Links

OSHWHub OpenSource (Chinese): [https://oshwhub.com/gloomyghost/yuzuki-lohcc-pro-usb-3-2-gen1-hdmi-huan-chu-cai-ji-ka](https://oshwhub.com/gloomyghost/yuzuki-lohcc-pro-usb-3-2-gen1-hdmi-huan-chu-cai-ji-ka)



