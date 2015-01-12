## GE Reflective Memory Custom Device with multiple DMA transfer ##

**It is only useful for interfacing with 3rd party systems, as NI VeriStand's built in GE RefMem support is vastly superior for communicating between NI VeriStand targets. Compare to native implementation, that does one DMA transfer per PCL, this custom device does multiple transfers based on memory locations. So the performance of communication with GE reflective memory is improved, when the addressed are distributed in multiple location. Detection change on write is also implemented. Multiple boards in the system are supported. Windows are also supported.**

!!!To install the support for this custom device you must copy the GE5565PIORC_NetworkInterrupts_DMA.inf  to :/ni-rt/system/ and reboot. !!!
!!!The support  for GE Fanuc in MAX can NOT be installed!!!

### LabVIEW Version ###

LabVIEW 2013 SP1

### Built Availability ###

No builds are available.

### Quality, Limitations ###

The IP was developed for one specific customer and was deployed successfully. 

### License ###

Copyright (c) 2015, National Instruments Corporation
All rights reserved.
Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
