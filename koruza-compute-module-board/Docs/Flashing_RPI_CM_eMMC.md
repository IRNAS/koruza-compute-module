# RPI CM Flash manual
The Compute Module has an on-board eMMC device connected to the primary SD card interface. This guide explains how to write data to the eMMC storage using a Compute Module IO board and Raspberry Pi 2B or 3B board.


1. Put the RPI CM in the RPI CM IO board socket. 
2. Set the J4 jumper (USB SLAVE BOOT ENABLE) on the RPI CM IO board to the EN.
3. Plug the micro USB power into the RPI 2B/3B. 
4. SSH to the RPI 2B/3B

*****
If the RPI 2B/3B is configured:

5. On RPI 2B/3B: `cd usbboot`
6. On RPI 2B/3B: `sudo ./rpiboot`
7. Now plug the host machine into the Compute Module IO board USB slave port (J15) and power the CMIO board on. The rpiboot tool will discover the Compute Module and send boot code to allow access to the eMMC. 
8. On RPI 2B/3B: `cd ..`
9. On RPI 2B/3B: `cd image`
10. On RPI 2B/3B: `sudo dd if=image_name.img of=/dev/sda bs=4MiB` Note the following command may take some time to complete, depending on the size of the image.
11. Make sure J4 (USB SLAVE BOOT ENABLE) is set to the disabled position and/or nothing is plugged into the USB slave port. Power cycling the IO board should now result in the Compute Module booting from eMMC.

*****
If the RPI 2B/3B is NOT configured:

5. On RPI 2B/3B: `sudo apt-get update`
6. On RPI 2B/3B: `sudo apt-get install git`
7. Git may produce an error if the date is not set correctly. On a Raspberry Pi, enter the following to correct this: `sudo date MMDDhhmm` where MM is the month, DD is the date, and hh and mm are hours and minutes respectively.
8. On RPI 2B/3B: `git clone --depth=1 https://github.com/raspberrypi/usbboot`
9. On RPI 2B/3B: `cd usbboot`
10. On RPI 2B/3B: `sudo apt-get install libusb-1.0-0-dev`
11. On RPI 2B/3B now build and install the usbboot tool: `make`
12. NOW CONTNOUE FROM THE **If the RPI 2B/3B is configured: number 6.** 

If you have problems configuring the RPI CM please check the [link][link1].

[link1]: https://www.raspberrypi.org/documentation/hardware/computemodule/cm-emmc-flashing.md
