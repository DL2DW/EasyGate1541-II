# EasyGate1541-II

![](https://github.com/DL2DW/EasyGate1541-II/blob/main/Images/EasyGate1541-II.jpg)



The EasyGate1541-II is also a replacement as a GateArray, similar to the [EasyGate1541](https://github.com/DL2DW/EasyGate1541). However, this version is designed for the Commodore 1541-II floppy drive.

I have currently implemented only the required routines for the 1541-**II**. Therefore this version cannot be used in the 1571. It is also not pin compatible to the "old" 1541!



## Assembly



The design is analogous to the first EasyGate1541, with two exceptions. First, there is another LED, which has no function in the current firmware, and the JTAG connector.

Since more pins are needed for the 1541-II, there were no more corresponding pins free for the JTAG connector.

So I just put SMD pads on the backside.

![](https://github.com/DL2DW/EasyGate1541-II/blob/main/Images/EasyGate1541-II_PCB_back.jpg)

To upload the firmware, I simply built an adapter with pogo pins. I simply soldered these to a pin header and then plugged them together with Dupont connectors and a piece of ribbon cable.



![](https://github.com/DL2DW/EasyGate1541-II/blob/main/Images/EasyGate1541-II-Firmware-Adapter.jpg)



Because the pads, due to the small space, do not correspond exactly to the grid size of 2.54mm, you have to press them minimally sideways a little bit, so that it fits.

Instead of pogo pins you can of course use a simple pin header. Here you just have to be more careful for the right contact. 

As a JTAG programming device I can recommend again a FT232H adapter, as it can be seen on the picture. With this adapter and the tool xc3sprog you can easily flash the firmware.

I recommend the following manual: https://github.com/1c3d1v3r/neatPLA/tree/master/programming



## BOM

Except for the CPLD, comparison types can also be taken.

| No#  | Designator | Part                            | Description                                |
| ---- | ---------- | ------------------------------- | ------------------------------------------ |
| 1    | U1         | MaxLinear SPX5205M5-L-3-3/TR    | Voltage regulator SOT-23-5                 |
| 2    | U2         | Xilinx XC9572XL-10VQG44C        | CPLD VQFP-44                               |
| 3    | D1         | Everlight 25-21/GHC-YSU/2A      | LED green, 1206                            |
| 4    | D2         | Everlight 25-21/BHC-XR2S1/2A    | LED blue, 1206                             |
| 5    | D3, D5     | Everlight 25-21/T1D-ANQHY/2A    | LED white, 1206                            |
| 6    | D4         | Everlight 25-21SURC/S530-A4/TR8 | LED red, 1206                              |
| 7    | C1 - C3    | Kemet C0603C104J4RACTU          | Capacitor, 100nF, 16V, X7R, 0603           |
| 8    | C4, C5     | Kemet C0805C106J8RACAUTO        | Capacitor, 10µF, 10V, X7R, 0805            |
| 9    | R1 - R5    | Yageo SR0603FR-7T1KL            | Resistor, 1k, 1%, 1/4W, 0603               |
| 10   | CN1, CN2   | Mill-Max 800-10-020-10-002000   | Pin Header, 20pin, precision, Pitch 2.54mm |



## Tests



Even if I have received some "well-meaning" letters that I should please test with various original games and hardware extensions, I must ask for understanding that I must unfortunately pass here.

I can only perform rudimentary tests. After all, this is a hobby project. To buy the various "tips" now would go beyond the scope. Apart from the time needed for the tests.

Therefore I would be pleased about feedback, if known "more sensitive" programs and hardware also run with the EasyGate1541-II.

Of course, I would also appreciate feedback if something doesn't run. Then this can be analyzed together if necessary.



## License

The contents of this repository is released under the following license:

- the "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License" (CC BY-NC-SA 4.0) full text of this license is included in the [LICENSE.CC-NC-BY-SA-4.0](https://github.com/DL2DW/EasyGate1541-II/blob/main/LICENSE.CC-NC-BY-SA) file and a copy can also be found at https://creativecommons.org/licenses/by-nc-sa/4.0/
