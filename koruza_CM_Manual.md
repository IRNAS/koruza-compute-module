# Koruza Compute Module board Manual

This document is dedicated to the Koruza CM board and all its features. 

## Introduction
Koruza CM board is the base board for the Raspberry Pi Compute Module CM1, CM3 and CM3Lite. The Raspberry Pi Compute Module (CM1), Compute Module 3 (CM3) and Compute Module 3 Lite
(CM3L) are DDR2-SODIMM-mechanically-compatible System on Modules (SoMs) containing processor, memory, eMMC Flash (for CM1 and CM3) and supporting power circuitry.

The CM1 contains a BCM2835 processor (as used on the original Raspberry Pi and Raspberry Pi B+ models), 512MByte LPDDR2 RAM and 4Gbytes eMMC Flash. The CM3 contains a BCM2837 processor (as used on the Raspberry Pi 3), 1Gbyte LPDDR2 RAM and 4Gbytes eMMC Flash. Finally the CM3L product is the same as CM3 except the eMMC Flash is not fitted, and the SD/eMMC interface pins are available for the user to connect their own SD/eMMC device.

Note that the BCM2837 processor is an evolution of the BCM2835 processor. The only real differences are that the BCM2837 can address more RAM (up to 1Gbyte) and the ARM CPU complex has been upgraded from a single core ARM11 in BCM2835 to a Quad core Cortex A53 with dedicated 512Kbyte L2 cache in BCM2837. All IO interfaces and peripherals stay the same and hence the two chips are largely software and hardware compatible.

All three versions of the Raspberry Pi compute module are supproted by the Koruza CM board.

## Features
Koruza CM board has many interfaces:
* GPIO Expansion header
  * IO pins
  * 2x UART
  * I2C
  * USB (Optional)
  * 2x SPI
  * PWM
  * Power
* Onboard 3 Amp DC to DC converter
* Upgrade software over USB
* MicroSC slot (Only for the Raspberry Pi CM3Lite moodule)
* Camera connetor
* Camera Enable Jumper
* 4x Host USB 2.0
* Ethernet 10/100 + PoE
  * Ethernet Bandwidth: 10Base-T/100Base-TX
  * 24VDC Passive PoE Input
* SFP Controle connector
* 24 VDC Power Input
* ESD protection for USB and Ethernet

## Block Diagram
![koruza_cm_block_diagram](https://github.com/IRNAS/koruza-compute-module/blob/board_1.x/pics/koruza_cm_diagram.png)

*Power module block is explained in section "Power supply"

## Mechanical Specification
The picture below shows the Koruza CM board dimension, cutouts and holes position. Holes dimensions are 3.2mm in diameter.

The maximum komponent height in the top side of the board is 14mm.

The maximum component height on the underside of the board is 2mm (component pins).

Note that the location and arrangement of components on the Koruza CM board may change slightly
over time due to revisions for cost and manufacturing considerations; however, maximum component
heights and PCB thickness and connectors positions will be kept as specified.

![koruza_CM_mechanical](https://github.com/IRNAS/koruza-compute-module/blob/board_1.x/pics/koruza_CM_mechanical.png)


## Power sypply
  ### Power Requirements
  
Exact power requirements will be heavily dependent upon the individual use case. If an on-chip subsystem is unused, it is usually in a low power state or completely turned off. For instance, if your application does not use 3D graphics then a large part of the core digital logic will never turn on and need power. This is also the case for camera, USB interfaces, video encoders and decoders, and so on.

Powerchain design is critical for stable and reliable operation of the Compute Module. We strongly recommend that designers spend time measuring and verifying power requirements for their particular use case and application, as well as paying careful attention to power supply sequencing and maximum supply voltage tolerance.

Recomended power input for the Koruza CM board is 24VDC 1A. 
  
  ### Power Diagram
  ![koruza_CM_power_diagram](https://github.com/IRNAS/koruza-compute-module/blob/board_1.x/pics/koruza_cm_power_diagram.png)
  
  
## Board peripherials
  ### Ethernet 
  
  ### USB Port
  ### Camera
  ### MicroSD Card
  ### UART Connector (Move Driver)
  ### Isolated FET output
  ### Front panle GPIO
  ### Expander GPIO connector
  
