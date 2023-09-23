# lightburn
Lightburn config and smoothieware configs for the laser cutter. Also some technical details of the hardware setup.

* config.txt is the Smoothieware config. Lives on the root of the removable media mounted from the MBED.ORG MBED USB DISK USB Device, along with the firmware that is being flashed to the device, if the flashing is sucsessful the firmware will be renamed FIRMWARE.CUR for FIRMWARE.BIN 
* prefs.ini is the Lightburn config. Lives in the C:\Users\Laser Cutter User\AppData\Local\LightBurn folder


## Summary of changes from stock Silvertail setup

* Faulty Proprietary controller board replaced with a Smoothieboard clone V1.0
* Extra microswitch endstop limit switches installed for X min, Y min.
* Replaced faulty Y max limit switch.
* ACnode now powers down the Smoothieboard controller by interrupting +5V power to it.
* Software on PC is now Lightburn rather than LaserCut53.
* No more dongle
* PWM output of the smoothieboard to control the laser power has been level-shifted to ensure a +5V PWM singal. Tests had shown that the PWM output was peaking at about +3.3V, which clearly had an effect on the laser power output.
