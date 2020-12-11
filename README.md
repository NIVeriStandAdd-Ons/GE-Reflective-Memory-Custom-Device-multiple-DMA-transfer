## GE Reflective Memory Custom Device with multiple DMA transfer ##

It is only useful for interfacing with 3rd party systems, as NI VeriStand's built in GE RefMem support is vastly superior for communicating between NI VeriStand targets. Compare to native implementation, that does one DMA transfer per PCL, this custom device does multiple transfers based on memory locations. So the performance of communication with GE reflective memory is improved, when the addresses are distributed in multiple location. Detection change on write is also implemented. Multiple boards in the system are supported. OS supported are Windows, Pharlap and LinuxRT.

**To install the support for this custom device on Pharlap you must copy the GE5565PIORC_NetworkInterrupts_DMA.inf  to :/ni-rt/system/ and reboot.
**To install the support for this custom device on Linux RT you must copy the GE5565PIORC_NetworkInterrupts_DMA.inf  to :/etc/nipal/devinit.d and reboot.
DO not install the GE Fanuc support files from MAX!!!**

This version removes all User Interface capabilities to add/remove DMAs/Channels. Configuration is only available via a text file (CSV file). There is one example of a configuration file coming with source code. Here are the column headers for the file:
*BlockName, Block Offset (Doubles), Block Direction (Read or Write), Channel Relative Offset (Doubles), Channel Name, Channel Unit, Channel Default Value (for Write Channels Only)*

Header |Definition
-------------	|-------------
BlockName  | It’s the DMA BlockName, same name for all Channels from that given Block.
Block Offset (Doubles)  | It’s the DMA Block Offset (in Doubles), same Offset for all Channels from that Block.
Block Direction (Read or Write)|It’s either “Read” or “Write”, no other values supported. All Channels from that block must be set to same Direction value.
Channel Relative Offset (Doubles)|It’s the Relative Offset of that Channel within considered DMA Block. For Read Direction, there might be gaps (addresses not used within the Block). For Write Direction all Offsets must be present.
Channel Name|NI-VeriStand Channel Name.
Channel Unit|Unit for that Channel. It can be omitted (empty string).
Channel Default Value (for Write Channels Only)|Value used as Init Value for that NI-VeriStand Channel. Note that it applies only for Write Direction. It can be omitted (empty string).


### LabVIEW Version ###

LabVIEW 2019

### Dependencies ###

VeriStand Dev tools VIPC: https://forums.ni.com/t5/NI-VeriStand-Add-Ons-Documents/VeriStand-Development-Tools-VIPC/ta-p/3632685

OpenG Toolkit:
http://sine.ni.com/nips/cds/view/p/lang/en/nid/209027


### Built Availability ###

No builds are available.

### Quality, Limitations ###

The IP has been updated for one specific customer and was deployed successfully.

**Determinism issues have been identified in this version of the custom device on NI Linux RT. Use the code in the 2020_pxiLinuxRt branch if losing data is not acceptable in your application.**

### License ###

*This repository and any materials provided by NI therein are provided AS IS. NI DISCLAIMS ANY AND ALL LIABILITIES FOR AND MAKES NO WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING WITHOUT LIMITATION ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR  PARTICULAR PURPOSE, OR NON-INFRINGEMENT OF INTELLECTUAL PROPERTY. NI shall have no liability for any direct, indirect, incidental, punitive, special, or consequential damages for your use of the repository or any materials contained therein.*
