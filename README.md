Please find the program of **Gateway** in the following link

<https://github.com/xuanjiao/ble_gateway>


## How to set up developing enviroment on Windows PC

1. Download [Microsoft Studio Code](https://code.visualstudio.com/) and install C/C++ extensions.

2. Download [Mbed Cli](https://github.com/ARMmbed/mbed-cli/blob/1.8.3/README.md) (Arm Mbed command-line tool) and export project to VS Code.

3. Download [GCC-ARM compiler](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads), [GNU Arm Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm) and [Make-3.81](https://sourceforge.net/projects/gnuwin32/files/make/3.81/) and change PATH system variable.

4. [Configuring the debugger](https://os.mbed.com/docs/mbed-os/v5.15/tutorials/visual-studio-code.html) and debugging my project **failed, error shows in figure**（leave it for now and use RTT for sinple debug instead). 


5. Build application in VS code using mbed.exe and generate .hex file.
![VS Code](./image/VSCode.png)


6. Download latest [Jlink Software Pack](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack) includes [Jlink FlashLite V6.54](https://www.segger.com/products/debug-probes/j-link/technology/flash-download/)
[RTT Viewer](https://www.segger.com/products/debug-probes/j-link/tools/rtt-viewer/). Use RTT Viewer to monitor information from MCU.

7. Erase the MCU and flash .hex file to MCU.

8. Download [nRF Connect](https://www.nordicsemi.com/Software-and-tools/Development-Tools/nRF-Connect-for-mobile) on Android smart phone to scan BLE devices

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

