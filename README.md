# tinyTorch #
https://github.com/JChristensen/tinyTorch  
https://github.com/JChristensen/tinyTorch-fw  
README file  
Jack Christensen Jan-2017

## Introduction ##

**tinyTorch** is a small LED flashlight controlled by an [ATtiny84A](http://www.atmel.com/devices/ATTINY84A.aspx) microcontroller. Choose white light for best illumination, or red light to preserve night vision. Eight brightness levels are selectable. The circuit can be programmed to power off automatically; two power-off intervals are available.

**tinyTorch** runs on two AA cells. Any type will work, including alkaline, standard carbon/zinc or rechargeable types (NiMH, NiCd). A boost regulator keeps the supply voltage and therefore the LED brightness constant as the batteries age. Because of the boost circuit, **tinyTorch** can run on batteries that will no longer power other devices, more nearly extracting all the energy available from the batteries. The microcontroller monitors the voltage and automatically shuts the circuit off when the batteries are exhausted to prevent leakage.

[Hardware design](https://github.com/JChristensen/tinyTorch) and [firmware](https://github.com/JChristensen/tinyTorch-fw) are available on GitHub.  
PC boards can be ordered from [OSH Park](https://www.oshpark.com/shared_projects/xy6vIOX3).  
A bill of materials is available at [Mouser Electronics](https://www.mouser.com/ProjectManager/ProjectDetail.aspx?AccessID=e556f7b439) and also as part of this repo.

## Operation ##

Press either button to turn **tinyTorch** on. The last color and brightness are remembered.
Press UP/COLOR to increase brightness; press DOWN/OFF to decrease.
Press and hold UP/COLOR to change between the white and red LEDs.
Press and hold DOWN/OFF to turn off.

To program **tinyTorch** to turn off automatically after one minute:
- Remove one battery.
- Press and hold the DOWN/OFF button.
- Insert the battery.
- Release DOWN/OFF.

To program **tinyTorch** to turn off automatically after five minutes, use the steps above but press and hold the UP/COLOR button instead.

To disable the automatic turn-off feature, use the steps above but press and hold both buttons instead.

When the batteries are exhausted, **tinyTorch** will blink the red and white LEDs alternately and then turn off. The brightness levels will be set to the minimum values. This may allow **tinyTorch** to continue to operate at a lower brightness level for a limited time but it is advisable to replace the batteries soon to prevent leakage.

## CC BY-SA ##
"tinyTorch" by Jack Christensen is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

![](https://github.com/JChristensen/tinyTorch/raw/master/board-sm.png)
