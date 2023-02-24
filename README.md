# BlackpillTE-INAV (FixedWing)
DIY Flight Controller and Firmware for Fixed Wing UAVs

* 108Mhz STM32F411CEU6
* MPU6500
* Magnetometer, Barometer, Rangefinder, Air speed
* GPS
* 2x UARTs, 2x Softserials, 2x SPIs, 1x I2C
* 2x Motors, 5x Servos Outputs
* SDCard Blackbox
* LED_strip
* PINIO1 and PINIO2


————————————————————————————————-

Flashing BF/INAV/Ardu firmware with STM32CubeProgrammer

https://www.st.com/en/development-tools/stm32cubeprog.html

You may download Windows version from here  en.stm32cubeprg-win64_v2.9.0.zip

————————————————————————————————-

Make sure DFU driver has been installed. Check out “Install DFU Drivers” in this page

Connect the FC USB to computer while holding the boot button in.

    Select USB
    USB1 and click Refresh
    Connect
    select “Erasing & Programming”
    Click “Full chip erase”
    Browse the hex or bin file from your computer, if flashing ardupilot, use “ardu*_with_bl.hex”.
    Click “Start Programming”
    After programming,  unplug USB and plug USB back in. FC will boot and run in normal COM mode.

![My Remote Image](https://github.com/EonClaw/BlackpillTE-INAV-FixedWing-/blob/main/stm32CubeProg-1.jpg?dl=0)

![My Remote Image](https://github.com/EonClaw/BlackpillTE-INAV-FixedWing-/blob/main/stm32CubeProg-2.jpg?dl=0)

————————————————————————————————-

Install DFU Drivers (DFU mode)

—Use one or the other of two—
Zadig 2.4

    Connect the FC USB to the PC While holding the boot button in. (DO NOT power on FC via external 5V or Vbat)
    Open Zadig
    Choose Options > List All Devices
    Select STM32 BOOTLOADER in the device list (if instead you see STM32 Virtual Com Port you are not in DFU mode – don’t replace the driver!)
    Choose WinUSB (v6.x.x.x) in the box on the right side of the green arrow and click Replace Driver
    Unplug FC from the computer
    Restart BF/INAV configurator
    Connect the FC USB to the PC While holding the boot button in.
    BF/INAV configurator should show it’s connected in DFU mode in the top right corner
    Choose the latest hex file for your FC and then “Load Firmware Online/local”. Once loaded, click “Flash Firmware”.

ImpulseRC Driver Fixer

    Start ImpluseRC Driver Fixer
    Connect the FC USB to the PC While holding the boot button in. (DO NOT power on FC via external 5V or Vbat)
    The ImpulseRC Driver Fixer should then see and load the proper driver
    Start BF/INAV configurator
    Connect the FC USB to the PC while holding the boot button in.
    BF/INAV configurator should show it’s connected in DFU mode in the top right corner (DO NOT click the CONNECT button)
    Choose the latest hex file for your FC and then “Load Firmware Online/local”. Once loaded, click “Flash Firmware”.

Install STM32 VCP Drivers (COM mode)

    STM32 Virtual Com Port driver   (Windows)
    STM32 Virtual Com Port driver X64  (Windows)
    PC devices manager should show “STMicroelectronics Virtual COM Port (COMxx)” if VCP drivers is installed successful.
     “FS Mode” is not suitable.
    If PC drivers manager doesn’t show right COM port,  uninstall it.
    Restart your computer. reinstall STM VCP drivers without FC connected.  then connect FC USB to the PC to see if COM port can be detected.

