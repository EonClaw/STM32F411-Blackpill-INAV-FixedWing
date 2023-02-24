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
