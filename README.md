# Creality CR-10S Pro hardware mods

### CR-10S Pro Custom Transfer Board

Customized [transfer board](Transfer_Board/) to allow maximum installation flexibility when using Duet3D control boards.  Note that this modified version **is NOT** compatible with [ribbon cable breakdown board (pt)](../RibbonCable_MB_BreakdownBoard_pt/), since several ribbon cable conductors have been relocated or re-purposed in order to separate all the signal and power lines.

ReXT3D fork changes v1.0 (April 2021):

- Removed the LED connector to free-up three ribbon cable conductors.  This allows fully independent signal routing and eliminates all shared grounds and power.
- Relocated connectors for slightly better clearances.
- Added a Z_MIN connector that shares wiring with the BL_TOUCH connector.  This allows use of the stock capacitive probe, or similar capacitive or inductive probes without a need for re-pinning.
- Widened the MOTOR and HEAT traces and doubled to both layers for improved current carrying capacity.
- Slightly widened all other traces.
- Relocated TH signal wires to the edge of the ribbon cable, away from “noisy” PWM signals such as heater or fans.

ReXT3D fork changes v1.1 (May 2021):

The original board design had an error in spacing of the two mounting post holes - they were almost a millimeter to close and would not allow the board to be mounted in the printer without filing or grinding one of the holes.  The ribbon cable connector was also incorrectly offset and would not allow the black metal cover to be installed without cutting an opening in it.  Unfortunately I found all of this out **<u>after</u>** I spent money on fabricating the boards and expensive expedited shipping.  Very disappointing, but my bad for not checking the dimensions first.  While correcting these issues, I made additional significant changes for v1.1.

  - Corrected the mounting post hole spacing error.
  - Increased the mounting post pad diameter.
  - Repositioned the ribbon cable connector to allow adequate cover clearance.
  - Increased board width to match the standard 57.5 mm width of the ribbon cable connector.
  - Corrected the ribbon cable connector footprint to include holes that allow mounting to the PCB.
  - Reduced minimum copper clearances in-line with OSHPark requirements, allowing for wider stepper motor traces.
  - Re-routed and widened all other traces once again.

<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/Transfer_Board/images/top.png" width="500">



#### Wiring example for Duet 3 Mini 5+

The following table provides complete wiring reference for Duet 3 Mini 5+ installation in the CR-10S Pro.  This includes all of the ribbon cable signals routed through the transfer board as well as all other printer interfaces.  This has been verified and fully function tested.

<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/Transfer_Board/images/duet3mini.png" width="500">



#### Ready made board

I ordered version 1.1 boards from JLCPCB as opposed to OSHPark to take advantage of their quick turnaround time and they did not disappoint - I received the finished boards in five days.  The following photos  show the top and bottom of the finished board next to the Creality OEM board, as well as the finished board installed in my printer.  Note that the installation photo is visually misleading and there is plenty of clearance between the board, the wiring and the lead screw.

*I have several bare PCBs on-hand that I would be willing to part with.  Contact me if interested.*



<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/Transfer_Board/images/finished-top.jpg" width="500">

<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/Transfer_Board/images/finished-bottom.jpg" width="500">

<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/Transfer_Board/images/finished-installed.jpg" width="500">



#### Firmware configuration

I only run Klipper firmware, even on the Duet boards.  My Klipper configuration is located at [[DGUS-reloaded-Klipper-config]](https://github.com/ReXT3D/DGUS-reloaded-Klipper-config/tree/personal-duet3mini5+).

The Creality DGUS touch screen flashed with Desuuuu's slick [DGUS-reloaded-Klipper](https://github.com/Desuuuu/DGUS-reloaded-Klipper) interface now works and has been fully tested with Desuuuu's [Klipper](https://github.com/Desuuuu/klipper) branch as of his May 26, 2021 commits.  Many thanks to Desuuuu for graciously implementing the changes required to allow fully configurable serial comms with Klipper's ATSAMD code.



### CR-10S Pro Duet 3 Mini 5+ Mounting Bracket

I designed a custom mounting bracket for the Duet 3 Mini 5+ control board.  The bracket picks-up on the existing CR-10S Pro enclosure mounting points, uses metal standoffs to avoid direct plastic contacts with a potentially hot PCB, and includes mounting for the stock blower fan with a fence that routes air over the bottom side of the PCB to correctly cool the TMC2209 stepper drivers.  More details are available on Thingiverse: [CR-10S Pro Duet 3 Mini 5+ Adapter Bracket](https://www.thingiverse.com/thing:4841999)

<img src="https://github.com/ReXT3D/cr-10s-pro-mods/raw/duet3d/CR-10S_Pro_Duet_3_Mini_5+_Mouning_Bracket/images/bracket-installed.jpg" width="500">