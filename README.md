# MB2K2_V0.90 release

Microbox 2K2 (MB2K2). 

The MB2K2 is a hardware based emulator built around the Xmos XU216 SoC where each of the 16 RISC cores in the SoC map onto the individual LSI chips of the system being emulated, CPU, PIA, ACIA, RTC etc. The PCB has VGA based video together with a PS/2 keyboard interface and USB for power and two virtual serial ports to a host computer. 

Initially I’ve used it to emulate an old 1982 era 6809/Flex single board computer design of mine (Microbox 2) but there’s nothing to stop the emulation of other processors and LSI devices by using a low cost JTAG interface and free toolchain from Xmos. If enough folks are interested I should be able to order a batch of blank PCBs.

The hardware is complete and the initial firmware supports:-

* MC6809 processor emulation running at approx 8MHz equiv (ie 4x faster than the original)
* 64KB of 6809 RAM with MON09 and Flex in ‘ROM'
* 200KB ramdisk + 1MB+ promdisk
* WD2123 DUART emulation with twin serial ports to the host computer as VCPs via USB, one can be used with FlexNet for remote storage
* MC146818 RTC emulation via a physical battery backed RTC/PRAM on the PCB
* MC6821 PIA emulation for the MB2’s bell and option switches and PS/2 keyboard interface (replaces the MB2’s parallel keyboard)
* uPD7220A hardware graphics accelerator emulation with output as 768x576 ‘VGA’
* PS/2 keyboard interface 

Not in the initial release but ‘hardware ready’ is a 3 1/2” floppy disk interface emulating the WD1770 FDC.

This all fits on a 80x80mm double sided 4 layer PCB which is designed to be assembled by hand (few fine pitch components etc).
