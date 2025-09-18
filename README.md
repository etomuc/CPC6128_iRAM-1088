# iRAM/1088 - and internal RAM expansion for Amstrad CPC 6128 (upgrade to 1088K) 

<img src="/pictures/iram1088a.jpg" width="400"/> <img src="/pictures/iram1088b.jpg" width="400"/>

## License

The expansion and all resources are free to use for personal use.

It is released under the same license as the [iRAM/640 project](https://github.com/etomuc/CPC6128_iRAM-640). The price for commercial offers may be adjusted to accomodate for the two SRAMs but must not exceed a 20% uplift compared to the permitted iRAM/640 prices. 

## Differences to iRAM/640

- provides 1088K of total RAM (64K base RAM + 1024 SRAM)
- the second 64K RAM bank of the 6128 is not used

The hardware differences are minimal:

* Use 2 SMD SRAMs AS6C4008 SOP32 (instead of 1 DIP SRAM)
* One more capacitor 100nF

## Building the iRAM/1088

### Disclaimer

> [!CAUTION]
>**USE AT YOUR OWN RISK.**
>
>This is a hobby project, I am a hobbyist and no engineer. There is always the risk that the expansion can cause harm to your CPC. 
>Although I have tested the expansion on several CPCs for many hours with many other expansions and lots of software, there is no guarantee that it will properly work under all circumstances, with all expansions or with all revisions of the CPC 6128.
>
> Especially if you are building this for others (commercially or not) make sure to make your own intense tests to guarentee this expansion works as expected before handing over to the recipients.  
>
>**USE AT YOUR OWN RISK.** 

- Get PCB from PCBWay here: https://www.pcbway.com/project/shareproject/CPC_iRAM_1088_1MB_internal_RAM_expansion_for_the_Amstrad_CPC_6128_ce7298f2.html
- or use the PCB gerber files that can be found in the files folder on this project. 
- CPLD programming files: please download the JED files from the files folder on the [iRAM/640 project](https://github.com/etomuc/CPC6128_iRAM-640). Those JED files already contain the required logic to address 1088MB. 

Otherwise please refer to the building instructions of the iRAM/640. The process is mostly identical except for two steps:

- the second SRAM needs to be soldered on the bottom side of the PCB
- make sure to close the 1MB bridge on the bottom side of the PCB

<img src="/pictures/iram1088bridge.jpg" width="600"/>

### 576K option

It's possible to only use a single SRAM which will give you a total of 576K RAM. 

- solder one SRAM on top of the PCB and leave the spot on thebottom side empty
- don't close the 1MB bridge on the bottom
- instead add the 10K (4.7K is also fine) resistor next to it
