# BLE gateway nRF52 DK

A gateway that communicate with light sensor modules via BLE, collect light value and calculate the probability of light on.

Link to the Raspberry Pi gateway program: [Raspberry Pi Gateway](https://github.com/xuanjiao/ble_gateway)

This project belongs to my old master thesis. It was not finished because during lockdown I was not able to go to the lab. Therefore I have started a new master thesis: robot scheduling

## Requirements

[nRF52 DK](https://www.nordicsemi.com/Software-and-Tools/Development-Kits/nRF52-DK)

[Microsoft Studio Code](https://code.visualstudio.com/) and its C/C++ extensions.

[Command line tool Mbed Cli](https://github.com/ARMmbed/mbed-cli/blob/1.8.3/README.md) 

[GCC-ARM compiler](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)

[GNU Arm Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm) 
 
[Make-3.81](https://sourceforge.net/projects/gnuwin32/files/make/3.81/) 

[Jlink FlashLite V6.54](https://www.segger.com/products/debug-probes/j-link/technology/flash-download/)

[RTT Viewer](https://www.segger.com/products/debug-probes/j-link/tools/rtt-viewer/).

[nRF Connect](https://www.nordicsemi.com/Software-and-tools/Development-Tools/nRF-Connect-for-mobile)


# Installation
```
git clone https://github.com/xuanjiao/ble_gateway.git
```

# Usage

1.  Change PATH system variable for make tool.

2.  Import project in VS Code.

3. Build application in VS code using mbed.exe and generate .hex file.

4. Use Jlink FlashLite to erase the MCU and flash .hex file.

5. Sse Android App nRF Connect scan BLE devices

6.  Use RTT Viewer to monitor information from MCU.

## Base station (NRF52_DK)Work flow 

![workflow_bs](./drawio_assets/work_flow_bs.png)

## Sensor information

CC2560 sensorTag User's guide <https://processors.wiki.ti.com/index.php/CC2650_SensorTag_User's_Guide>

### Light sensor

- **version** OPT3001. <http://www.ti.com/lit/ds/symlink/opt3001.pdf>
- **unit** Illuminance(lux) <https://en.wikipedia.org/wiki/Lux>
- **examples of the illuminance provided under various conditions:**
    ![lux](./image/lux.PNG)

### Movement sensor

- **version** MPU-9250 <https://invensense.tdk.com/products/motion-tracking/9-axis/mpu-9250/>

