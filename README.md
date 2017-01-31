# tinyTorch #
http://github.com/JChristensen/tinyTorch  
ReadMe file  
Jack Christensen Jan 2017

## Introduction ##

A small LED torch controlled by an ATtiny84A microcontroller. The user can choose white light for best illumination, or red light to preserve night vision. Eight brightness levels are selectable. The circuit can optionally power down automatically; two power-down intervals are available. The circuit monitors the battery voltage and automatically shuts down when the battery is exhausted to prevent cell leakage.

Firmware is available [on GitHub](http://goo.gl/VueLrD).  
PC boards can be ordered [from OSH Park](https://www.oshpark.com/shared_projects/ASV7G4qa).  
A Bill of Materials with Mouser part numbers is part of this repo.

## Operation ##

## Circuit Details ##

The circuit runs on two AA cells; either alkaline or rechargeable types (NiMH, NiCd) will work. The board is sized to fit on the back of a Keystone no. 2462 battery holder.

The circuit uses a boost regulator to keep the supply voltage and therefore the LED brightness constant as the battery ages. The microcontroller monitors the regulator output voltage and shuts the circuit down (power down sleep mode) to prevent over-draining the batteries and possible leakage.

## CC BY-SA ##
"tinyTorch" by Jack Christensen is licensed under [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).

![](https://raw.githubusercontent.com/JChristensen/ledFire_HW/master/board1.jpg)
  
![](https://raw.githubusercontent.com/JChristensen/ledFire_HW/master/board2.jpg)
