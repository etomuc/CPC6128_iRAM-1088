# iRAM/1088 - and internal RAM expansion for Amstrad CPC 6128 (upgrade to 1088K) 

<img src="/pictures/iram1088a.jpg" width="400"/><img src="/pictures/iram1088b.jpg" width="400"/>

## Differences to iRAM/640

- provides 1088K of total RAM (64K base RAM + 1024 SRAM)
- the second 64K RAM bank of the 6128 is not used

The hardware differences are minimal:

* Use 2 SMD SRAMs AS6C4008 SOP32 (instead of 1 DIP SRAM)
* One more capacitor 100NF

## Building the iRAM/1088

- PCB gerber files can be found in the files folder on this project. 
- CPLD programming files: please download the JED files from the files folder on the [iRAM/640 project](https://github.com/etomuc/CPC6128_iRAM-640). Those JED files already contain the required logic to address 1088MB. 

Otherwise please refer to the building instructions of the iRAM/640. The process is identical except for one step:

- make sure to close the 1MB bridge on the bottom side of the PCB

<img src="/pictures/iram1088bridge.jpg" width="400"/>
