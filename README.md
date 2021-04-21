# Creality CR-10S Pro hardware mods
### Boards
[Ribbon cable breakdown board](RibbonCable_MB_BreakdownBoard/) - is fully compatible with original transfer board, helps with wiring with non-original motherboards without any changes to the Creality stock ribbon cable.

changes from fork:

- Beefed up trace width where possible. 
- Heater PCB trace has trace on both Front and Back.
- Heater connector changed to  a more standard 5.08mm screw terminal
- and added I2C AT24C256 EEPROM 

<img src="https://github.com/SkullKill/cr-10s-pro-mods/raw/master/RibbonCable_MB_BreakdownBoard/images/RibbonCable_MB_BreakdownBoard-Front.jpg" width="500">

<img src="https://github.com/SkullKill/cr-10s-pro-mods/raw/master/RibbonCable_MB_BreakdownBoard/images/RibbonCable_MB_BreakdownBoard-Front-BoardOnly.jpg" width="500">





[Ribbon cable breakdown board (pt)](RibbonCable_MB_BreakdownBoard_pt/) - "pig tail" soldering oriented, semi compatible with original transfer board, but fully compatible with [Transfer board](Transfer_Board/). Has dedicated 4-wire connection for BLTouch and 3-wire connector for LED.

<img src="https://raw.githubusercontent.com/darknode/cr-10s-pro-mods/master/RibbonCable_MB_BreakdownBoard_pt/images/top.png" width="250">





[Transfer board](Transfer_Board/) - clean transfer board.  Note that this modified version **is NOT** directly compatible with [Ribbon cable breakdown board (pt)](../RibbonCable_MB_BreakdownBoard_pt/), since a number of ribbon cable conductors have been relocated and/or re-purposed.  The purpose of these changes was to separate all the signal lines, allowing maximum installation flexibility when using Duet3D control boards.

ReXT3d changes from fork (April 2021):

- Removed the LED connector to free-up three ribbon cable conductors.  This allows fully independent signal routing and eliminates all shared grounds and power.
- Relocated connectors for slightly better clearances.
- Added a Z_MIN connector that shares wiring with the BL_TOUCH connector.  This allows use of the stock capacitive probe, or similar capacitive or inductive probes without a need for re-pinning.
- Widened the MOTOR and HEAT traces and doubled to both layers for improved current carrying capacity.
- Slightly widened all other traces.
- Relocated TH signal wires to the edge of the ribbon cable, away from “noisy” PWM signals such as heater or fans.

<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/Transfer_Board/images/top.png" width="250">

#### Wiring examples
*Coming soon*

#### Ready made boards
*Photos coming soon*
