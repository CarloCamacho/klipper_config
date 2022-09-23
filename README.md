Welcome to my 3D Printer configuration repo. 


| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/creality.png" width="150">| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/klipper-logo.png" width="150">  | <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/mainsail.png" width="150">   |  <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/fluidd.PNG" width="150"> | <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/BTT.jpg" width="150"> | 
| :------------:| :------------: | :------------: | :------------: | :------------: |
| [Creality CR-10v3](https://www.creality3dofficial.com/products/creality-cr-10-v3-3d-printer-with-genuine-e3d-direct-drive-extruder-2020-latest-version "Creality CR-10v3")| [Klipper](https://www.klipper3d.org "Klipper")  | [Mainsail](https://docs.mainsail.xyz/ "Mainsail")  | [Fluidd](https://docs.fluidd.xyz/) | [SKR Mini E3 v3](https://www.biqu.equipment/products/bigtreetech-skr-mini-e3-v2-0-32-bit-control-board-for-ender-3 "SKR Mini E3 v3")  |

## Please note, this is a work in progress! 

The Creality CR-10v3 is a great base to build on while getting to know the electronics and motion control systems of 3D printers.  I am using this to experiment with different hotends, extruders and control boards with the aim of eventually building something from kit. Eg. Voron, RatRig. 

Above are the main hardware and software components I am working with and have basic functionality working. 

The CR-10 had an external control box that housed the PSU, control board and LCD, with cables running to small breakout boards on the printer itself.
I've found the small breakboards to be a bit flakey when adjusting wiring, etc so I am in the process of doing a control box delete which means I am running the board, power and wiring off the bench currently until I confirmed everything is working.  

I am running klipper on a Raspberry Pi 4 Model B 4GB which is sharing its duties with a few other functions around the house including:
- HomeAssistant
- Zigbee2Mqtt

I ended up going with the Fluiddpi image as I found it the simplest to get up and running with any extra bloat. 

I am also running the fantastic [Kiauh](https://github.com/th33xitus/kiauh) scripts to keep everything up-to-date.  It's been perfect for installing and testing the different interfaces. 

## General Notes so far:
- I used the sample config from Klipper GitHub for the SKR and it worked well out the box
- The config checker page in the doco was a great help
- I had to change the direction of the Extruder stepper motor initially
- All motion and control seems to be working great! 

## Next Steps:
- ~~Wiring - make the PSU safe...~~
- ~~Bed levelling / Bed Mesh~~
- ~~Do an actual test print~~
- ~~Mounting PSU / SKR / Pi somewhere~~
 - ~~Print PSU holder~~
 - ~~Print mount/case for the rest. Possibly on the Skadis?~~
- Hotend changes
 - ~~Print new mount for extruder (HeroMe Gen6)~~
 - ~~Install LDO Orbitor 2.0~~
 - ~~Install replacement heater cartridge & thermistor~~
 - ~~Install BL-Touch~~
 - ~~Rewire hotend to remove reliance on daughterboard...~~
 - ~~Cable management~~


## Update - August 2022
Alright, so i've got through the list above and everything basically went to plan. 
I've removed the control box completely and run everything directly to the BTT board with no screen. (I use Fluidd for everything)
The mount and placement of the PSU mimics the Ender 3 approach which works well. (See last image)
I've mounted the SKR on a board on the side for easy access to cables - its not the neatest, but its worked well, particularly when testing different parts and configurations.
The BL-tocuh is mounted and working well too. 
I ended up mounting the bearing based spool holder on the Skadis pegboard. 
All up i'm really happy with the Orbitor and Dragon hotend combo, its been able to print everything that i've thrown at it well.
The last part i'm going to look to change on this printer will likely be the bed material.
The glass is ok, great in fact, for PLA... but PETG and others I end up using glue and painters tape. 
I'll likely get a PEI based sheet I can switch out.

## Tips:
- Get yourself some good tools if you plan to do a lot of work on a 3D Printer 
- eg. various crimpers, wire strippers, and hex drivers are a must 
- The HeroMe mount system is fantastic - highly recommend joining the Patreon to get the latest designs and guides if you aren't doing anything with linear rails.  
- Ikea Skadis peg boards are just awesome to have close for those tools you bought...


## Images:

| Almost the original system with the control box visible. |
| :------------: |
| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/controlbox.jpg" width="450">  |
| Wiring in Progress  |
| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/wiring.jpg" width="450">  |
| Starting Hotend - Phaetus Dragon HiFlow w/ BMG clone extruder.   HeroMe Gen5 mount.  |
| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/BMGHotend.jpg" width="450">  |
| Final form - Phaetus Dragon HiFlow w/ LDO Orbitor 2.0.   HeroMe Gen6 mount.    |
| <img src="https://github.com/CarloCamacho/klipper_config/blob/master/images/orbitor.jpg" width="450">  |


### End
