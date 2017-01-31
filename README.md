# tinyTorch #
http://github.com/JChristensen/tinyTorch  
ReadMe file  
Jack Christensen Jan 2017

## Introduction ##

**tinyTorch** is a small LED torch controlled by an ATtiny84A microcontroller. The user can choose white light for best illumination, or red light to preserve night vision. Eight brightness levels are selectable. The circuit can optionally power off automatically; two power-off intervals are available. A boost regulator keeps the supply voltage and therefore the LED brightness constant as the batteries age. The microcontroller monitors the voltage and automatically shuts down when the battery is exhausted to prevent cell leakage.

**tinyTorch** runs on two AA cells; either alkaline or rechargeable types (NiMH, NiCd) will work.

[Hardware design](https://github.com/JChristensen/tinyTorch) and [firmware](https://github.com/JChristensen/tinyTorch-fw) are available on GitHub.  
PC boards can be ordered [from OSH Park](https://www.oshpark.com/shared_projects/xy6vIOX3).  
A bill of materials is available at [Mouser Electronics](https://www.mouser.com/ProjectManager/ProjectDetail.aspx?AccessID=e556f7b439) and also as part of this repo.

## Operation ##

Press either button to turn **tinyTorch** on. The last color and brightness are remembered (unless the batteries have been removed.)
Press UP/COLOR to increase brightness; press DOWN/OFF to decrease.
Press and hold UP/COLOR to change between the white and red LEDs.
Press and hold DOWN/OFF to turn off.

To set **tinyTorch** to turn off automatically after one minute:
- Remove one battery.
- Press and hold DOWN/OFF.
- Insert the battery.
- Release DOWN/OFF.

To set **tinyTorch** to turn off automatically after five minutes, use the steps above but use the UP/COLOR button instead.

To disable the automatic turn-off feature:
- Remove one battery.
- Press and hold either button for 2-3 seconds.
- Release the button.
- Insert the battery.

When the battery is exhausted, **tinyTorch** will blink the red and white LEDs alternately and then turn off. The brightness levels will be set to the minimum values. This may allow **tinyTorch** to continue to operate at a lower brightness level for a limited time but it is advisable to replace the batteries soon to prevent leakage.

## CC BY-SA ##
"tinyTorch" by Jack Christensen is licensed under [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).

![](https://raw.githubusercontent.com/JChristensen/ledFire_HW/master/board1.jpg)
  
![](https://raw.githubusercontent.com/JChristensen/ledFire_HW/master/board2.jpg)
