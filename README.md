# tinyTorch#
http://github.com/JChristensen/tinyTorch  
ReadMe file  
Jack Christensen Jan 2017

## Introduction ##

A small LED torch with two colors and eight brightness levels. 

Firmware is available [on GitHub](http://goo.gl/VueLrD).  
PC boards can be ordered [from OSH Park](https://www.oshpark.com/shared_projects/ASV7G4qa).  
A Bill of Materials with Mouser part numbers is part of this repo.

## Circuit Details ##

The circuit is meant to run on two AA cells; either alkaline or rechargeable types (NiMH, NiCd) will work. Battery life with two fresh alkaline cells is over 50 hours continuous with three LEDs installed on the board. The board is sized to fit on the back of a Keystone no. 2462 battery holder.

I use high-brightness LEDs with clear lenses. I only populate three LEDs, two yellow and one red. This worked well for my application. Adding the fourth LED will reduce battery life somewhat but the MCU has four PWM outputs so it is there as an option (the firmware drives all four).

The circuit uses a boost regulator to keep the supply voltage and therefore the LED brightness constant as the battery ages. By default, the regulator supplies 3.3V, but this can be changed to 5V via a solder jumper.

The MCU monitors the supply voltage and once the battery has been exhausted to the point where the regulator cannot supply the proper voltage, the MCU shuts down the circuit and goes into low-power sleep mode. The MCP1640 boost regulator has the ability to operate with less than one volt input; this can drain the battery to the point where the cells leak, so the shutdown mechanism is implemented in an effort to prevent this.

The cutoff voltage for the shutdown is selected by another solder jumper; the board is strapped for a 3V cutoff by default (to correspond to the regulator being set for 3.3V). If the regulator is changed to 5V, the cutoff should be changed to 4.5V using the jumper. Having said that, I see little use for operating the circuit with a 5V supply voltage as it will reduce battery life, but it was easy enough to implement at no extra cost (well, one resistor). A 5V supply will also likely require different values for the LED current-limiting resistors.

## CC BY-SA ##
"LED PWM Fire Effect" by Jack Christensen is licensed under [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).

![](https://raw.githubusercontent.com/JChristensen/ledFire_HW/master/board1.jpg)
  
![](https://raw.githubusercontent.com/JChristensen/ledFire_HW/master/board2.jpg)
