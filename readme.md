# Opencore Hackintosh in Intel - ASUS

## PC components
* | Type | Description |
  | ---- | ----------- |
  | CPU | Intel Core i7-9700K |
  | GPU | Intel UHD 630 Graphics (No dGPU required) |
  | Motherboard | ASUS Maximus XI Hero (Wi-Fi) (Chipset z390) |
  | RAM | HyperX DDR4 2 x 16GB @ 3466MHz |
  | SSD | Samsung EVO Plus 500GB SSD M.2 |
  | PSU | Corsair RMx 850W |
  | Display 1 | MSI Optix MPG341CQR - 3440x1440 @ 120Hz (DisplayPort 1.2) |
  | Display 2 | ASUS TUF VG32V - 2560x1440 @ 60Hz (HDMI 1.4b) |

## Requirements
* [OpenCore 0.6.6](https://dortania.github.io/OpenCore-Install-Guide/)
* [Hackintool 3.5.3](https://github.com/headkaze/Hackintool/releases/latest/download/Hackintool.zip)

## Kext used in this build
* AirportItlwm
* AppleALC
* IntelBluetoothFirmware
* IntelBluetoothInjector
* IntelMausi
* Lilu
* NightShiftUnlocker
* SMCProcessor
* SMCSuperIO
* USBInjectAll
* VirtualSMC
* VoodooHDA
* WhateverGreen

## Installation
* This repo contain the files required on `EFI/` folder to install a macOS in a PC with the [components](#pc-components) listed above, you should copy them in a USB with FAT32 format alongside `com.apple.recovery.boot/` folder.
* In order to get the macOS image installation, please follow this Dortania's [guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/#creating-the-usb).
* After install, we'll get **macOS** installed, in my case I got **macOS 10.15 Catalina** and after that I got new updates in order to upgrade a new macOS version.


## Displaying dual monitor
* By default, the motherboard's displayport is the main display, and probably the HDMI port will be ignored when a monitor is connected, using Hackintool we can fix this.
* For that, just follow the configuration that you can see in the next images:
    * Check the macOS version in **Framebuffer** menu option:

        If you have Big Sur 11.2.1, check as the image. If you have a previous version than 10.13.6, check the second one.
        
        <img src="./img/img1.png" width="80%">
    * In **Patch** menu option check `Apply Current Patches`.

        In **System Configs** we must select the motherboard brand that we have, but in my case I couldn't find it, I tried selecting `Asus > TUF Z390-Pro Gaming [CFL]` which have a similar architecture as mines.

        <img src="./img/img2.png" width=80%>

    * In `Patch` we must check the options as follows:

        <img src="./img/img9.png" width=80%>
        <img src="./img/img10.png" width=80%>
        <img src="./img/img11.png" width=80%>

        After that, restart the Mac.
    * Once you restarted the Mac, you might see your seconday monitor enabled using HDMI port.

        Open Hackintool and make sure that you can see this next:

        <img src="./img/img3.png" width=80%>
        <img src="./img/img4.png" width=80%>
        <img src="./img/img5.png" width=80%>
        <img src="./img/img6.png" width=80%>
    * Display settings in Mac should look like this:

        <img src="./img/img7.png" width=90%>
## Complete
* Now, enjoy using Mac !

    <img src="./img/img8.png" width=80%>