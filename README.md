Welcome to 3D Printer configuration repo. 


| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/creality.png" width="150">| <img src="https://www.klipper3d.org/img/klipper-logo.png" width="150">  | <img src="https://raw.githubusercontent.com/mainsail-crew/docs/master/assets/img/logo.png" width="150">   |  <img src="https://avatars.githubusercontent.com/u/38851044?v=4" width="150">
| :------------:| :------------: | :------------: | :------------: |
| [Creality CR-10v3](https://www.creality3dofficial.com/products/creality-cr-10-v3-3d-printer-with-genuine-e3d-direct-drive-extruder-2020-latest-version "Creality CR-10v3")| [Klipper](https://www.klipper3d.org "Klipper")  | [Mainsail](https://docs.mainsail.xyz/ "Mainsail")  | [SKR Mini E3 v3](https://www.biqu.equipment/products/bigtreetech-skr-mini-e3-v2-0-32-bit-control-board-for-ender-3 "SKR Mini E3 v3")  |

## Please note, this is a work in progress! 

The Creality CR-10v3 is a great base to build on while getting to know the electronics and motion control systems of 3D printers.  I am using this to experiment with different hotends, extruders and control boards with the aim of eventually building something from kit. Eg. Voron, RatRig. 

Above are the main hardware and software components I am working with and have basic functionality working. 

I am in the process of doing a control box delete on this CR10 which means I am running the board, power and wiring off the bench currently until I confirmed everything is working.

I am running klipper on a Raspberry Pi 4 Model B 4GB which is sharing its duties with a few other functions around the house including:
- HomeAssistant
- PiHole
- OctoPrint (now disabled)

So far memory usage and CPU are handling it all fine, but I have a spare Pi3 handy if I need to move it off. 

The main consideration with the other services running on the PI is the ports for all the web interfaces. A summary is below for my record and failing memory...

| Fluidd  | Port  |
| :------------: | :------------: |
| Fluidd  | 8111  |
| Mainsail  | 8222  |
| Moonraker  | 7125  |
| OctoPrint |  5001  |
| HomeAssistant  | 8213  |
| PiHole  | 80  |

Note: I have listed Fluidd and OctoPrint above, but it was mostly for testing - I am finding Mainsail to be my go to interface.  YMMV

## General Notes so far:
- I used the sample config from Klipper GitHub for the SKR
- The config checker page in the doco was awesome
- I had to change the direction of the Extruder stepper motor
- All motion and control seems to be working great! 

## Next Steps:
- Wiring - make the PSU safe...
- Bed levelling / Bed Mesh
- Do an actual test print
- Mounting PSU / SKR / Pi somewhere
 - ~~Print PSU holder~~
 - Print mount for the rest. Possibly on the Skadis?
- Hotend changes
 - Print new mount for extruder (HeroMe Gen6)
 - Install LDO Orbitor 2.0
 - Install replacement heater cartridge & thermistor
 - Rewire hotend to remove reliance on daughterboard...


 Images:

Wiring in Progress
<img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/wiring.jpg" width="150">

Starting Hotend - Phaetus Dragon HiFlow w/ BMG clone extruder.   HeroMe Gen5 mount.
<img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/BMGHotend.jpg" width="150">




###End