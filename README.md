# lightburn
Lightburn config and smoothieware configs for the laser cutter. Also some technical details of the hardware setup.

* config.txt is the Smoothieware config. Lives on the root of the removable media mounted from the MBED.ORG MBED USB DISK USB Device
* prefs.ini is the Lightburn config. Lives in the C:\Users\Laser Cutter User\AppData\Local\LightBurn folder

## TODO

- [ ] Clean and align optics
- [x] ~~Control panel to improve the user interface, specifically for focusing the beam.~~
- [ ] Nail down configs, or at least make them easy to restore.
- [x] ~~Buy lightburn licence (paid, awaiting licence key)
- [ ] Install lightburn licence (Dean) 
- [ ] get lightburn addional seat licences (Dean)
- [x] ~~Prevent the MBED.ORG MBED USB DISK from automatically showing
- [x] ~~Work out how to get the acnode logging laser run time~~ reliably
- [ ] Tidy panel wiring and terminate cabling properly.
- [ ] Tidy USB and network cabling to prevent footstep damage.
- [ ] Differences documentation for existing lasercutter users
- [ ] Training for new lasercutter users
- [ ] Enjoy

## Summary of changes from stock Silvertail setup

* Faulty Proprietary controller board replaced with a Smoothieboard clone V1.0
* Extra microswitch endstop limit switches installed for X min, Y min.
* Replaced faulty Y max limit switch.
* ACnode now powers down the Smoothieboard controller by interrupting +5V power to it.
* Software on PC is now Lightburn rather than LaserCut53.
* No more dongle
* PWM output of the smoothieboard to control the laser power has been level-shifted to ensure a +5V PWM singal. Tests had shown that the PWM output was peaking at about +3.3V, which clearly had an effect on the laser power output.
