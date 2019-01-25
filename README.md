# ESP32_WROVER_BREAKOUT

## Features
* Breadboard compatible connector spacing
* TPS82140  switched-mode power supply - Vinmax 17V, Vout 3.3V @ max 2A, Iq ~20uA
* TPS3839 voltage supervisor keeps ESP32 in reset if supply voltage drops below threshold. This is useful when you have a large capacitor on the 3.3V power supply that discharges slowly. Use TPS3839K33DBZ for a voltage threshold of ~2.93V.
* Solder jumper to select between external regulated 3.3V supply or TPS82140 output.
* Schematic and board layout using Kicad 5.0.2 on Ubuntu 18.10 amdx64
* Gerber files generated using instructions at https://support.jlcpcb.com/article/44-how-to-export-kicad-pcb-to-gerber-files
* PCB layout designed for hand soldering
  * vias in pads, no thermal relief on pads. 
  * Use low-temperature solder for TPS82140, this will make it easier and safer to reflow with a DIY process, e.g. electric skillet. 
  * There's no need to risk damage to the ESP32-WROVER module by reflow-soldering it. Just apply thermal grease (not solder paste) on the ESP32-WROVER ground pad before soldering the castellated-edge pins.

## Credits
ESP32-WROVER footprint and component library from https://github.com/aliafshar/esp32-wrover-kicad
