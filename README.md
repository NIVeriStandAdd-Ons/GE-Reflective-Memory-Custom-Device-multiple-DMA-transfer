## GE Reflective Memory Custom Device with multiple DMA transfer ##

**It is only useful for interfacing with 3rd party systems, as NI VeriStand's built in GE RefMem support is vastly superior for communicating between NI VeriStand targets. Compare to native implementation, that does one DMA transfer per PCL, this custom device does multiple transfers based on memory locations. So the performance of communication with GE reflective memory is improved, when the addresses are distributed in multiple location. Detection change on write is also implemented. Multiple boards in the system are supported. Windows are also supported.**

**To install the support for this custom device you must copy the GE5565PIORC_NetworkInterrupts_DMA.inf  to :/ni-rt/system/ and reboot.
The support  for GE Fanuc in MAX can NOT be installed!!!**

### LabVIEW Version ###

LabVIEW 2013 SP1

### Dependencies ###

VeriStand Dev tools VIPC: https://forums.ni.com/t5/NI-VeriStand-Add-Ons-Documents/VeriStand-Development-Tools-VIPC/ta-p/3632685

### Built Availability ###

No builds are available.

### Quality, Limitations ###

The IP was developed for one specific customer and was deployed successfully. 

### License ###

*This repository and any materials provided by NI therein are provided AS IS. NI DISCLAIMS ANY AND ALL LIABILITIES FOR AND MAKES NO WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING WITHOUT LIMITATION ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR  PARTICULAR PURPOSE, OR NON-INFRINGEMENT OF INTELLECTUAL PROPERTY. NI shall have no liability for any direct, indirect, incidental, punitive, special, or consequential damages for your use of the repository or any materials contained therein.*
