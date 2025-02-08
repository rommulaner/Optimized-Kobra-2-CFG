# Optimized-Kobra-2-CFG
Tool to UPLOAD and DOWNLOAD the printer configuration to the USB Stick and modified settings for a 9x9 bedmesh, quicker leveling and probing in the centre of the bed
How to:
1. Download the ZIP that fits to your printer.
2. Unzip the files and put all 4 files into the root folder of the USB stick (FAT32).
3. Plug the USB stick in any USB slot of the printer.
4. Go to the print menu and select the UPLOAD gcode file and hit PRINT to upload the config to your printer (current settings will be overwritten)
   If you want to save the current config you need to select the DOWNLOAD gcode file and print it. Then the files on the USB stick will be overwritten with the current settings of the printer.
   Dont' forget to store the downloaded settings somewhere and replace the config files again if you want to upload the optimized settings afterwards.
   NOTE: In order to print the file the filament sensor needs to be deactivated or filament needs to be loaded, like on a regular print, otherwise you will get an error message.
6. After uploading the new config you need to power cycle the printer to load the new config.
7. With the new config the whole calibration needs to be done (Sensor calibration, Input Shaping, Autoleveling) as everything of this is at stock stettings.
   Note: Do the calibration steps as written above, because Input Shaping calibration can lead to missing steps during the test and the sensor calibration doesn't perform a homing of all axis before the probing and this will mess up the sensor calibration values
   Tip: Heatup the bed manually and let it stay for about 10 minutes before doing the autoleveling to get a better heat distribution and better leveling results
8. Now you have a 9x9 bedmesh with no interpolation inbetween the probed points as Klipper results in overshoots if the bedmesh is higher than 6x6. Also the probing is bit quicker to save some time and the z probing is done in the centre of the bed

Attention!
Changing values in the config by yourself can lead to bricked mainboard with no way back if you are not sure what you are doing!
Especially if you change the values of the probed bedmesh at the end of the config file.
I only changed the interpolation values there from 3,3 to 0,0 and the printer didn't startup after that.

Thanks to the Discourse group that found this door to the Kobra 2 firmware and espacially daksimpson for sharing this gcodes.

Happier Printing!
