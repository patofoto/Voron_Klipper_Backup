
![DEMON](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/c2bae2ee-be37-48ea-b6ac-c2c32e661751)
 
# Welcome to 3DPrintDemon DEVILISHLY GOOD Klipper macros!

The very latest UNIFIED version for these macros! Huge re-implementation &amp; new Features!

[<img width="171" alt="kofi_s_tag_dark" src="https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/08473899-563b-4b4d-9409-5e6602d6ec44">](https://ko-fi.com/3dprintdemon)

**Made to make your printing life easier & your printer SMARTER!**

I hope you enjoy these automatic & highly adaptive macros! Don't forget if you like & use this project you can buy me a beer/coffee to say thanks. https://ko-fi.com/3dprintdemon
A lot of time, testing, love & coffee has been poured into them!
If you feel you’d like to support my efforts & help to enable me to continue sharing my ideas please consider buying me a beer/coffee at the provided “Sponsor this project” link. Thanks!



# This UNIFIED version will run on almost any COREXY or BED SLINGER (cartesian) Klipper printer with no changes needed to the macro files! 
Small user setting changes will be required of course.

These macros have been developed for use on almost anything from Voron printers to an Ender3, & anything else in between! They will check what sort of machine you have & try to adapt themselves to it automatically!

So for example if you hit `MACHINE_LEVEL` on a COREXY printer you'll get a `QUAD_GANTRY_LEVEL`, but if you do the same on a bed slinger you'll get a `Z_TILT_ADJUST` - if your printer has that feature enabled! Plus now once the new variable `use_manual_levelling` is enabled that same macro button wil provide you `bed_screws` or `screws_tilt_calculate` functions & bypass any auto levelling calls! Same macro button but different function! Also there is a built in smart park, where the printer knows if you have a probe based Z endstop or a switch & will adjust the parking height during macro events to suit your system! Further hardware options are manually selectable in the user settings file.

Checks & Error Handling. This is a big problem for many users, you get an error in klipper but its written in "code" so you cant tell what it means! Here I have tried to explain all errors that occur while running the macros clearly. Sadly I cant help the "encoded" system ones! They'll still be hard to read!

# These macros rely on you setting the correct filament type in your slicer! BE SURE YOU DO THIS!

*NOTE: This version is a totally new approach to these macros & therefore have only been tested on my machines, while every effort has been made to make sure they work well there could well be a few bugs that need squashing! So please be sure to report anything that doesn't work correctly or errors you come across. However if you're able please try to solve the issue yourself first & let me know your solution so I can merge it. Thanks all!*

# Sept 10th Component update:
- Added `LOAD` & `UNLOAD` macros to the pack, no longer any need to manually add them [see here](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified?tab=readme-ov-file#klipperscreen-loadunload-macros)
- Added encoder filament sensor support for filament `LOAD`/`UNLOAD` macros
- Added encoder filament sensor support for filament `LOAD_CLEAN` & `UNLOAD_CLEAN` macros
- Updated all filament `LOAD` & `UNLOAD` macros to use feedrate mm/s as per Mainsail `Extruder` interface
- Added safety limit for `max_extrude_only_velocity` during filament loading/unloading
- Updated [encoder filament sensor macro](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified?tab=readme-ov-file#filament-sensor)
- Updated `demon_user_settings.cfg` to include mesh selection options for `AUTO MESH BUILDER` macro
- Added mesh selection options to the `AUTO MESH BUILDER` macro
- Added safety lock-out for `LOAD_CLEAN` & `UNLOAD_CLEAN` macros so can't be used while printing
- Added sefety lock-out for `PRESENT_TOOLHEAD` & `STOW_TOOLHEAD` macros so can't be used while printing
- Added Nevermore Post Print features, see the `demon_user_settings.cfg` file!

# VERSION 2.8 LATE UPDATE!!!
- NEW! Added support to use KAMP Adaptive Purge & Smart Park macros! Install fork KAMP_LiTE to use!
- Added BLTouch parking height
- Updated Github docs
- Updated demon_user_settings file

- if you've already download v2.8 please does so again & backup your old files including your `demon_user_settings_v2.8.cfg` file as you'll need to transfer your settings over.

# NEW for Version 2.8!!!
- Better more efficient Klicky actions when Klicky probe is used as Z endstop. 
- More efficient conditional homing during start for inductive probe printers
- More efficient nozzle cleaning during start for inductive probe printers
- Improved Auto E-stop setup, requires unused pin & relay/ssr/transistor connected to the probe's power
- Improved encoder runout sensor handling! Now the encoder will be disabled until layer 2 of the print job!
- General small macro improvements & tweaks to core assets & more.
- Added heat soak skip option
- Added disable macro flow rate adjustment options
- Added option to turn off neopixels at the end of the print or leave them on
- Added option to skip drawing purge lines if you want - good for when you have an uneven bed & like to use Adaptive Meshing
  
- NEW FEATURE MACRO - Added chamber heater control options!
- NEW FEATURE MACRO - Added Manual Levelling support for Bed Screws & Screw Tilt Adjust!

- Modified chamber temperature variable naming
- Chamber temperature min/max settings now available per filament type!! Not just 2 values for all anymore!
- Bed Fans macro big update with Floating Bed Fans improvements
- Bed Fans Floating fans calculates temperature mid points & allows fully interactive runtime adjustments to speed values
- Bed Fans thermal & power info display macros added
- The Full PID macro now auto saves at the end of the test
- The Auto Mesh Builder macro now auto saves all meshes at the end of the building process

- The system can now automatically detect which correctly setup chamber sensor you have, chamber sensor or chamber fan

# Previous & Existing Features

- NEW! ORCA Slicer `Multi_Surface` handling! 
- The printer knows what bed surface you choose to use & can add a pre-set Z offset for the print & remove it afterward! The system can even combine the surface offset with a filament or temperature based one! Don't worry though there are `Bed Saver` safety checks that should help stop you entering a wrong number & damaging your printer, especially when using the combine offset function!

- NEW! Random nozzle cleaning movements! 
- No more single path cleaning to wear out your brush/pad! All movements are randomly generated!

- NEW! Random filament purge parking! 
- No more purging in the same spot over & over piling filament on top of filament!

- NEW! Now includes the Demon Bed Fans Monitor!
- NEW! Now with Floating fan chamber control! The system will raise or low fan speed depending on temperature!
- Smart & fully adaptive Bed Fans control system!
- Full instructions available here in the `bed_fans.cfg` file

- NEW! The Demon AES System! 
- Save your printer from damage from homing errors when using a Z Endstop switch & Sensorless homing! This could save you a lot of money if homing fails!
- Full instructions available here: https://github.com/3DPrintDemon/Voron_2.4_AES_System_Auto_Emergency_Stop_For_Z_Endstop_Switch

- NEW! Start Macro handling for Smart Filament Sensor Encoder
- Disables the sensor until the macro completes

- NEW! Support for Klipper's `ADAPTIVE_MESH` system in the latest Klipper update
- NOTE you need the latest version of Klipper to use this!

If you own a Sovol SV06/Plus with a Sovol Klipper screen or a Sovol SV07/Plus & want to use the latest version of Klipper with Adaptive Meshing & more features you need to follow my How2 guide on how to update the Sovol Klipper screens on your printers.

https://github.com/3DPrintDemon/How-to-Update-Sovol-Klipper-Screen-To-Latest-Klipper-SV06-and-SV07 

- NEW! Adaptive Pressure Advance Mode! - APA - ORCA SLICER ONLY

- Why have only 1 single setting for Pressure Advance trying to work across the whole print when you can have 6!!

- 6 settings per filament, 30 in total!

- Each setting is automatically selected by filament for different types of extrusions during the print.

- Settings for Perimeter, External Perimeter, Internal Infill, Solid Infill, Top Solid Infill, & filament default.

- Print tuning towers for the speed of each extrusion type & apply them to the Adaptive Pressure Advance (APA) modifiers!

- Disable or enable individual modifiers, you don't have use them all, use any number in any combination!

- Or disable modifiers by filament or the whole module at once!

- All settings in one easy to edit place, no need to edit macro code!

- Verbose mode, read back all APA commands to the console!

***These macros rely on you setting the correct filament type in your slicer! BE SURE YOU DO THIS!***

**Mesh Auto Builder!**

- Auto build all 5 meshes at different temperatures with included heat soak waits & message prompts! Inspired by a community contribution from Karl L! Thank you for sharing!


**Demon Print Start End**

- The printer knows what filament you sliced your print for!

- You can now choose 2 different flow rates for each filament that are automatically selected depending on if you're using a small layer height for fine detail prints, or a large layer height to get stuff done quick for that filament! - LOVE THIS! 

- Pressure Advance & Smooth Time values for each filament, each can will be applied automatically, if the filament type is unrecognised the default stored value is used.

- Pre print filament runout check 

- Fast & adaptive Nozzle Preheat, values for each of the 5 filament presets. If the filament you're using is not on the list then the macro falls back on reading the file temps & makes a decision from there.

- Fully conditional homing, don't home again if you don't have to!

- If you have a chamber or printer enclosure with a temperature sensor the macro can be set to use it for heat soaking the printer.

- If you have a chamber or printer enclosure with a cooling fan then there are settings for when the fan comes on for each filament to help maintain the correct temperature!

- Store 5 Meshes, one for each filament type. Each will be called automatically for the correct filament! Then if the filament type is not recognised the macro will fall back on reading the file temps & makes a decision from there.

- Automatically applied high temperature expansion offset for ASA & ABS filaments with a bed-saver safeguard! You set the offset to use. This will only allow small adjustments so can't dig trenches into your bed! Range of -0.1mm to +0.1mm is available. Anything outside this range causes an Emergency Stop! Offset adjustment feature can be switched on/off. USE WITH CARE!

- PETG Anti-Squish with bed-saver safeguard! This allows a positive Z offset to all PETG prints automatically to reduce the first layer squish. Range 0.00 to +0.1mm. Anything outside this range causes an Emergency Stop! Offset adjustment feature can be switched on/off. USE WITH CARE!

- Filaments have Heat Soak timers that are now controlled by either enclosure temp sensor readings, or timers. You choose! Timers are default if you don't have an enclosure or sensor.

- Support for Quad Gantry Level on CoreXy machines & for 5 stepper driver bed slinger systems with Z-Tilt option

- Customise your purge line! Choose where to start & which axis to purge along! X or Y! 



**Demon User Settings**

- This file contains all the 'Variables' available for the Demon Print Start End Macro, open & edit one single file! No need to trawl through the macros!

- You can even turn on/off hardware options as your system changes & grows over time! Don't worry about future-proofing, its already built right in!



**Included User executable macros:**

- `PRINT_START`
- `PRINT_END`
- `_RET_CALI_START`
- `_GOODNIGHT`
- `Gantry_Level_Hot`
- `Gantry_Level_Cold`
- `CLEAN_NOZZLE`
- `LOAD_CLEAN`
- `UNLOAD_CLEAN`
- `Pressure_Advance_Test_Mode`
- `Auto_Bed_Mesh_Builder`
- `Stepper_Buzz_Cycle`
- `PID_Tune_Mode_FULL`
- `Auto_Shaper_Calibrate`
- `Resonance_Test_X`
- `Resonance_Test_Y`
- `System Sensors`
- `Printer_Status`
- `Z_Switch_Calibrate_Hot`
- `Z_Probe_Calibrate_Hot`
- `Z_Probe_Accuracy_Hot`
- `Z_Switch_Calibrate_Cold`
- `Z_Probe_Calibrate_Cold`
- `Z_Probe_Accuracy_Cold`
- `Present_Toolhead`
- `Return_Toolhead`
- `Timer_Start`
- `Timer_Stop`
- `Power_Down`
- `Backup_Printer`
- `Bed_Fans_Speed`

- Plus many more automated ones!



****************************************************************************************************************************

# Introduction

These macros are smart & have adaptive properties & will shape themselves to what you’re printing. 
For example the macros know if your printer is CoreXY or bed slinger, they know if it's already homed so wont home it again, & can not only automatically shape itself to simple things like your printer’s bed size & what temperatures you’re printing at! Plus it can automatically choose & load the correct mesh for the temperature of your print, as your bed will slightly change shape the hotter it gets. 

Not only that but it will choose the correct settings for your chamber cooling system, & it will even check to see if you have filament loaded before starting a print! …We’ve all done that one haven’t we, be honest!!

Also it can decide if your chamber needs to be heat soaked or not before the print starts! This is fantastic for saving time, money & electricity between back-to-back prints where the system doesn’t require heat soaking as it’s already up to temperature!! 

You have all this plus step by step adaptive on screen messages on any Mainsail web interface & KlipperScreen system so you know exactly what your machine is deciding to do at any time! Some macros can be customised by changing the settings in the macro button options before you manually call the macro in the Mainsail or KlipperScreen interfaces!

It doesn't end there, as all these features are user customisable within the `demon_user_settings_v2.8.cfg` file! Some functions can be totally deactivated entirely & bypassed with a simple changing an option from `True` to `False`! This is very useful if your printer doesn’t have the hardware components installed at this time but leaves the configuration easily customisable with a few keystrokes in the future if you want to add to your machine!

With the `_GOODNIGHT` macro you can even flick a GUI switch in Mainsail to let the printer know you want it to auto power down after it’s finished printing!! 
This can be done at ANY point during the print! You can even change your mind & cancel the auto shutdown at any point before the print completes!

**NOTE: Additional hardware & setup is required for this feature to work! How to do this is explained further on in this readme file.**

**Retraction Calibration...**
The `_RET_CALI_START` macro is used when calibrating your retraction settings with files generated at:

http://www.retractioncalibration.com/

All you need do is paste `_RET_CALI_START` into the website's "Custom Gcode" box next to the green "Generate Gcode" button
This is without a doubt the absolute BEST retraction test out there!

**Nozzle Cleaning & Purge Buckets...**
The `CLEAN_NOZZLE`, `LOAD_CLEAN`, & `UNLOAD_CLEAN` macros are for use with a nozzle cleaning brush found here:

For VORON 2.4 printers
https://www.printables.com/model/201999-nozzle-scrubber-with-a-little-bucket-for-voron-24

For SV08 Printers
https://www.printables.com/model/873006-sovol-sv08-silicone-nozzle-cleaner-purge-bucket-mi
 
****************************************************************************************************************************
## All sounds great right!? Ok well here’s the tricky bit! 
…Well its not that tricky because I got it all written down here for you to just copy/paste into your setup!

**PLEASE CHECK ALL INSTRUCTIONS CAREFULLY & FOR ANY FILE SPECIFIC INSTRUCTIONS PLEASE CHECK THE FILE TEXT!**

**Don’t just install & run the macros & wonder why they don’t work! They WILL need setting up once on your system. Damage to your machine may result if the macros are run without the prerequisites or without the correct setup before first use!** 

You will need to edit your slicer's `Start G-code` & `End G-code` boxes to get the `PRINT_START` macro to work correctly. 

There are full instructions further down this page & the basic lines in the `demon_print_start_end_v2.8.cfg` file.

****************************************************************************************************************************

# Prerequisites
You must download & `[include]` these additional files along with these Demon Macros or they will NOT work correctly.

These additional macros are prerequisites:

### **FOR ALL MACHINES FOR ADAPTIVE PURGING & SMART PARK install KAMP_LiTE fork.**
- https://github.com/3DPrintDemon/KAMP_LiTE/releases/tag/v1.0

### **For VORON PRINTERS or other machines with toolhead Neopixels**
- https://github.com/VoronDesign/Voron-Stealthburner/blob/main/Firmware/stealthburner_leds.cfg
- https://github.com/rkolbi/voron2.4/blob/main/non-blocking_wait.md
  
###### Note: You will need to edit any entry in this file of "SET_LED LED=nozzle" to read "SET_LED LED=sb_leds"

###### Note: This file is requred for the heat soaks to work correctly. Install even if you dont have any LEDs & set a dummy pin.

### **For SOVOL SV08 PRINTERS**
- https://github.com/3DPrintDemon/Voron-Stealthburner/blob/main/Firmware/RGB_LEDs.cfg
- https://github.com/3DPrintDemon/Non_Blocking_Wait/releases/tag/Heat_Soak_Timers_V1.0
  
###### Note: This file is requred for the heat soaks to work correctly. Install even if you dont have any LEDs & set a dummy pin.

### **For other machines without toolhead Neopixels**
- https://github.com/3DPrintDemon/Non_Blocking_Wait/releases/tag/Heat_Soak_Timers_V1.0
  
###### Note: This file is requred for the heat soaks to work correctly. Install even if you dont have any LEDs & set a dummy pin.

You must keep neopixels set to `False` in the `demon_user_settings_v2.8.cfg` `Hardware Options` section





****************************************************************************************************************************
### IF YOU RAN V1.0-V2.7 BE SURE TO UPDATE YOUR SLICER'S START GCODE OR NEW FEATURES WONT WORK!
**Instructions to do this are further down this page.**
**Also you must update ALL the macro files as this new version will NOT work correctly with old files!**
****************************************************************************************************************************

**If you own a Sovol SV06/Plus with a Sovol Klipper screen or a Sovol SV07/Plus & want to use the latest version of Klipper with Adaptive Meshing & more features you need to follow my How2 guide on how to update the Sovol Klipper screens on your printers.**

https://github.com/3DPrintDemon/How-to-Update-Sovol-Klipper-Screen-To-Latest-Klipper-SV06-and-SV07 
****************************************************************************************************************************

# INSTALL THE MACROS MANUALLY

Copy the files here into a folder called `Demon_Klipper_Essentials_Unified` in your config folder on your printer. 

###### NOTE: If you download the zip file via the button at the top of the repo your downloaded folder will be called:
```
Demon_Klipper_Essentials_Unified-main
```
You must delete the `-main` part of the name so it reads `Demon_Klipper_Essentials_Unified` ONLY. 

Then copy that renamed folder to your printer.

Then, paste into your printer.cfg
```
[include ./Demon_Klipper_Essentials_Unified/*.cfg]
```

This will include all files in a folder called Demon_KLIPPER_Essentials_Unified in your `~/config` folder.
****************************************************************************************************************************

# INSTALL THE MACROS VIA SSH TO CLONE THE REPO DIRECTLY

Use Putty or MacOS Terminal to log into your system via SSH

```
cd /home/pi/printer_data/config
```
###### NOTE: the above command is for a real Raspberry Pi, if you're using a cloned system that "/pi" folder will change to `mks` or `btt` or `sovol` or similar.

```
git clone https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified.git
```

Then, paste into your printer.cfg
```
[include ./Demon_Klipper_Essentials_Unified/*.cfg]
```

This will bring these files into your system, be sure to comment out & NOT delete your current START & END PRINT Macros just yet!


****************************************************************************************************************************

# Macro Layout Import/Restore

Lastly in Mainsail click the cogs top right of the screen & then click the `RESTORE` button in the `Interface Settings` window under the `General` tab. Now find the `backup-mainsail-DEMON-MACROS.json` file, click open & then select the macros option, then click `Restore` to bring in the macro setup.

This will bring in the defualt macro layout. 

It will not change your toolhead layout, you will need to do this yourself if you wish to. This is done by changing the `Style` option in the `Control` tab of the `Interface Settings` window to `Circle`.

![Macro Layout](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/8a3d41e8-3cd3-4366-bab4-56cb790b3f29)



****************************************************************************************************************************

# Mainsail.cfg Usage

**This is for parking the toolhead when you pause or cancel a print.** 

You should be sure to `[include mainsail.cfg]` as we will be using this! 

You need to open the `Mainsail.cfg` file, select & copy the `[gcode_macro _CLIENT_VARIABLE]` & paste it all into a new editable `my_macros.cfg` file for example, as that `Mainsail.cfg` is read only & you can't make any changes to it.

Once pasted into the new file uncomment the `[gcode_macro _CLIENT_VARIABLE]` macro by selecting the whole macro & pressing `ctrl+/` on PC or `cmd+/` on MacOS.

Then setup where you want/need the park position, the extruder retract/unretract movements & speeds etc. You can even define two locations if you wish, one for pause, & one for cancel.

Now were it says `variable_user_pause_macro : ""` you need to paste in...
```
_Z_RAISE
```
Between the quote marks so it looks like this: `"_Z_RAISE"`

Now do the same for `variable_user_cancel_macro: ""`

Also be sure to add the line below for the `variable_runout_sensor: ""` option between the quote marks ("").
```
filament_switch_sensor filament_sensor
```
Your new uncommented `_CLIENT_VARIABLE` marco should look like this when you're done. Image is for a Voron 2.4 350

BE SURE TO SAVE & RESTART!



![Mainsail Client_Vars](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/6adea304-0697-43a9-81f9-4e352637f1d3)

****************************************************************************************************************************

# Define Respond Section

These macros make use of the `respond` command so please make sure your printer.cfg has this defined for use in the system. This is command is already defined in the your `Mainsail.cfg` that you just included above, so if you set these macros up correctly you wont need to add it, however if you choose not to use the `Mainsail.cfg` you will need to add the section manually.

```
[respond]
```

****************************************************************************************************************************


# Klipperscreen LOAD/UNLOAD Macros


###### NOTE: Klipperscreen Macros copy/paste into file is no longer required. Any previous copies of these LOAD/UNLOAD macros must be removed from any additional macro.cfg files in favour of the new included LOAD/UNLOAD macros. If you do not do this then there will be issues with the loading & unloading of filament.

All load & unload macros now check the printer's `max_extrude_only_velocity` setting, a value of 20 or below will pass the check. 

Be sure your `printer.cfg` file `[extruder]` section contains...

```
max_extrude_only_velocity: 12
```

****************************************************************************************************************************


# Printer Lights (White LEDs)
Be sure to name any White LEDs that are on an output_pin in the `printer.cfg` file you wish the macros to control to:

```
[output_pin Printer_Lights]
```
****************************************************************************************************************************


# Neopixel Toolhead LEDs 

....if using a Voron or another machine with neopixel LEDs in the toolhead. Be sure to name any neopixel toolhead LEDs:

```
[neopixel sb_leds]   
```
Or you will get an invalid for LED error.

....If you're using an SV08 leave the neopixel LEDs their defualt name:
```
[neopixel Screen_Colour]
```
If you have more than 3 neopixel LEDs in your chain be sure to correctly edit the file you're using to include all LEDs in the chain. By default it is set for 3 Stealthburner style toolhead LEDs.
You will need to change this if you have a long chain or use neopixels elsewhere on your printer.


![LED Chain Settings](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/d452e81e-5847-4b16-a752-760f587ffc4d)


****************************************************************************************************************************


# IF YOU'RE USING A SV08 PRINTER! 

If you are using anyhting else jump down a section to Adaptive Meshing.

YOU MUST, I REPEAT MUST DISABLE ALL THE SOVOL MACROS BY COMMENTING OUT THE macro.cfg FILE INCLUDE IN THE printer.cfg FILE! 
To do this use a # at the start of the line like this:
```
# [include Macro.cfg]
```
Then set your fans like this in the printer.cfg file:
```
[multi_pin fan_pins]
pins: extra_mcu:PA7, extra_mcu:PB1

[fan]
pin:multi_pin: fan_pins
max_power: 1.0
```
Comment out the stock entry do not delete it, it must look like this:
```
# [fan_generic fan0] # back model cooling fan
# pin: extra_mcu:PA7
# max_power: 1.0

# [fan_generic fan1] # front model cooling fan
# pin: extra_mcu:PB1
# max_power: 1.0
```

You will also need to go into the `printer.cfg` & comment out line 440 in the `[idle_timeout]` section.
```
# gcode: _IDLE_TIMEOUT
```
If not you will get an error when the the printer times out for unknown command as the macro its calling is disabled.

****************************************************************************************************************************

# Setting up KLIPPER's Adaptive Mesh option. 

There is no longer any need for a separate KAMP install for meshing. The adaptive purge line & smart park are still needed.

For Klipper's Adaptive Mesh feature to work you must have:
- You must have a version of Klipper later than 1st Feb 2024
- Enabled your Slicer for `Label Objects`
- It's good to have `Exclude Objects` too...
- Added the `file_manager` section to your `moonraker.conf` file for `object processing`  
- Added the `Exclude Object` section to your `printer.cfg` file

###### Find options under Orca main window Process/Global/Others

![ORCA Label](https://github.com/user-attachments/assets/1a1cd72e-11d9-4023-bc6e-ef0e0b9e0a9a)

Add this to your `moonraker.conf` file:
```
[file_manager]
enable_object_processing: true
```

Add this to your `printer.cfg` file:
```
[exclude_object]
```

Save & restart!

****************************************************************************************************************************

# Setting up KAMP_LiTE Adaptive Purge & Smart Park

KAMP_LiTE is simply KAMP but without the adpative meshing macro, as it is not required now klipper has Adaptive Meshing included by default. However the Adpative Purge & Smart Park features are still very useful! Changes listed in the link.

You must have a version of Klipper later than 1st Feb 2024. You must have completed the steps described in the above section.

Also the fork KAMP_LiTE must be installed & included, how to do this is in the below link:

https://github.com/3DPrintDemon/KAMP_LiTE/releases/tag/v1.0


You must set your desired values in the KAMP_Settings.cfg

![KAMP_LiTE Settings](https://github.com/user-attachments/assets/3ecfcd1c-b117-43b8-b8cb-9121be6c7b95)

Then you must activate the KAMP settings in the `demon_user_settings_v2.8.cfg` file.

![KAMP_LiTE Vars](https://github.com/user-attachments/assets/58ebc555-2bad-465c-b052-04c9f189171d)


To use correctly ensure your `extruder` section in your `printer.cfg` has the line below defined & that its set to 5 or higher, if not the KAMP purge will be skipped & it wont work!
```
max_extrude_cross_section: 5
```


###### NOTE: If `variable_adaptive_meshing` is set to `True` then the system will override the values for `variable_use_kamp_adaptive_purge` & `variable_use_kamp_smart_park`. It will always use the adaptive purge & smart park features no matter what the settings are. Even if they're set to false. User control is handed back once `variable_adaptive_meshing` is set to `False`


****************************************************************************************************************************
**To use adaptive meshing all files MUST have been sliced with `Label Objects` active.** 
IF NOT YOU WILL RECEIVE THE FOLLOWING ERRORS!!

If you use ORCA SLICER:

`Error evaluating 'gcode_macro PRINT_START:gcode': gcode.CommandError: This error is caused by the sliced file not having "Label Objects" enabled! Please disable Adaptive_Meshing in the demon_user_settings.cfg or re-slice the file with it enabled and restart the print!`

If you use another slicer:

`Internal error on command:"PRINT_START"`

`Internal error on command:"BED_MESH_CALIBRATE"`




****************************************************************************************************************************
# BE SURE TO SET YOUR MACRO VARIABLES & WATCH THIS VIDEO

- Configure the macros in one place! Set the variables for all the Demon Klipper Essentials macros in the `demon_user_settings_v2.8.cfg` file
- There is no need to edit any macro code with this macro pack!
- NOTE: If you don't set `_CLEAN_VARIABLES` the printer will give you an error if you haven’t done this & try to use the nozzle clean macros.

![Set Your Vars](https://github.com/user-attachments/assets/d2efa6c8-70c2-4585-aab3-08a4e29b6f0d)





**BE SURE TO WATCH THIS WHILE YOU SET UP YOUR MACROS...**

<a href="http://www.youtube.com/watch?feature=player_embedded&v=s4poVSt5a2g
" target="_blank"><img src="http://img.youtube.com/vi/s4poVSt5a2g/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="480" height="360" border="10" /></a>

Long video on settings walkthrough: https://youtu.be/s4poVSt5a2g


****************************************************************************************************************************
# SLICER SETUP

You have to modify your slicer's `Machine Gcode` that is sent to the printer.
The basic commands to do this are in the macro files, the expanded setup for use with Orca slicer is shown below, please take special care to copy them in correctly, as even a single error can stop the whole system from working.
Below shows a fully setup slicer as per recommended Mainsail settings combined with the macro settings for Orca Slicer using relative extrusion.

Cut/paste your current gcode out of the gcode window & into Notepad/Notes to save if you ever revert back & need it again. Replace your old Start gcode with the correct one for your slicer.
the example below is for Orca slicer. 
It's very important the last line of the `Machine Start Gcode` is a single long line as shown below, with no returns in it. 
If this is not the case the system will fail as soon as you start a print.

###### NOTE: If your screen can't hold the text in a single line the computer will place it on mulitple lines itself, however there will not be actual "returns" placed into it, as far as the printer will see it will still be one long line.

Here is how they should look in Ocra Slicer. 

![Orca Slicer Printer Gcode](https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/89453292-ce82-4c43-9df4-85430d7fe39b)

These are fully setup codes as per recommended Mainsail settings combined with the macro settings for Orca Slicer using relative extrusion, as per the image....

Machine Start G-code:

```
SET_PRINT_STATS_INFO TOTAL_LAYER=[total_layer_count]
M104 S0
M140 S0
PRINT_START EXTRUDER=[nozzle_temperature_initial_layer] BED=[hot_plate_temp_initial_layer] LAYER=[layer_height] FILAMENT=[filament_type] EXCLUDE=[exclude_object] SURFACE="[curr_bed_type]"
```
Machine end G-code:
```
; printing object ENDGCODE
PRINT_END
```

Before layer change G-code:
```
;BEFORE_LAYER_CHANGE
;[layer_z]
G92 E0
```

After layer change G-code:
```
;AFTER_LAYER_CHANGE
;[layer_z]
SET_PRINT_STATS_INFO CURRENT_LAYER={layer_num + 1}
M117 Layer {layer_num+1}/[total_layer_count] : {filament_settings_id[0]}
```

Change filament G-code:
```
PAUSE
```

Change extrusion role G-code:
```
_ADAPTIVE_PA TYPE=[extrusion_role]
```

Pause G-code:
```
PAUSE
```


**Fin...**

****************************************************************************************************************************

# Additional Configuration - EXTRA STEPS



## Chamber Monitoring & Fan Control

To get the most from these macros you’ll need to add a Chamber thermistor to your machine if you haven’t already & a Chamber exhaust fan. 
- If you have a Chamber exhaust fan call it `[temperature_fan chamber]`
- If you instead have a Chamber Thermistor only & no Exhaust fan call it `[temperature_sensor Chamber_Temp]`

****************************************************************************************************************************

## Printer LED lights
- If you have printer LED lights (NOT neopixel) call them `[output_pin Printer_Lights]`
- NeoPixel LEDs are dealt with in the additionally installed files.

****************************************************************************************************************************

## Filament Sensor
If you have or are going to install a filament sensor this must be added to your `printer.cfg` file to run the filament sensor. The filament runout check in the `PRINT_START` macro can then be enabled & disabled in the `_START_VARIABLES` marco if you dont have one or dont want to perform the check at the start of the print.
```
[filament_switch_sensor filament_sensor]
switch_pin: ^### <<<<<< Insert board pin for sensor
pause_on_runout: True
insert_gcode:
    { action_respond_info("Insert Detected") }
runout_gcode:
    { action_respond_info("Runout Detected") }
pause_delay: 0.5
```

If you have an encoder based sensor like the BTT Smart Sensor add this:
```
[filament_motion_sensor encoder_sensor]
 switch_pin: ^### <<<<<< insert board pin
 detection_length: 9
 extruder: extruder
 pause_on_runout: False
 insert_gcode:
     { action_respond_info("Filament Encoder is Running") }
 runout_gcode:
    { action_respond_info("Filament Encoder Stall Detected") }
    {% if printer.print_stats.state == "printing" %}
      PAUSE
    {% endif %}

 [delayed_gcode encoder_sensor]
 initial_duration: 1
 gcode:
    SET_FILAMENT_SENSOR SENSOR=encoder_sensor ENABLE=0
```

****************************************************************************************************************************

## Modifying KlipperScreen Menus For New Features
To add main screen menu buttons to KlipperScreen for your new Nozzle cleaning functions add these lines to your `KlipperScreen.conf` file:
```
[menu __main custom]
name: Prepare
icon: klipper

[menu __main custom present]
name: Present Toolhead
icon: bed-level-t-r
method: printer.gcode.script
params: {"script":"present_toolhead"}

[menu __main custom load]
name: Load Clean
icon: arrow-down
method: printer.gcode.script
params: {"script":"load_clean"}

[menu __main custom unload]
name: Unload Clean
icon: arrow-up
method: printer.gcode.script
params: {"script":"unload_clean"}

[menu __main custom clean]
name: Nozzle Clean
icon: shuffle
method: printer.gcode.script
params: {"script":"clean_nozzle"}

[menu __main custom stow]
name: Stow Toolhead
icon: bed-level-b-l
method: printer.gcode.script
params: {"script":"stow_toolhead"}

[menu __main custom ready_up_pla]
name: Ready Up PLA
icon: filament
method: printer.gcode.script
params: {"script":"ready_up_pla"}

[menu __main custom ready_up_asa]
name: Ready Up ASA
icon: filament
method: printer.gcode.script
params: {"script":"ready_up_asa"}

[menu __main custom ready_up_petg]
name: Ready Up petg
icon: filament
method: printer.gcode.script
params: {"script":"ready_up_petg"}
```
The icons are appropriate if you use with the material-darker theme. Other theme’s icons may differ.

You can also add your chamber temp to the menubar in KlipperScreen, this to your `KlipperScreen.conf` file:
```
titlebar_items: chamber
```

****************************************************************************************************************************

# Auto Shutdown Moonraker Power Device

To make use of the `_GOODNIGHT` post print auto shutdown macro you must enable your RPI as a secondary MCU so it can control your shutdown relay hardware. Use this link to do that.

- https://github.com/Klipper3d/klipper/blob/master/docs/RPi_microcontroller.md

After you've followed the process in that link be sure that this is added to your `printer.cfg` file.
```
[mcu host]
serial: /tmp/klipper_host_mcu
```

## Word of warning! Adding a power control device like a power shutdown relay can sometimes involve working with & modifying your printer’s wiring that runs on mains level voltage!  This can be extremely dangerous with a definite risk of serious injury, fire, loss of property & even death! You have been warned. I accept no liability or responsibility for any loss, death or injury caused directly or indirectly by you or anyone else attempting this! This is all on you, attempt implementation ENTIRELY AT YOUR OWN RISK!

## Connections

Example below for using the BTT Power Relay v1.2

See the install instructions for this product on the BTT Github! 

- https://github.com/bigtreetech/BIGTREETECH-Relay-V1.2

However….

This link is far more helpful! 

- https://www.youtube.com/watch?v=5wJff-hY90s

You will need ensure that you have set your instance to be able to control your Pi’s GPIO pins as mentioned previously in this document. Then you need to choose which 2 GPIO pins on your Rpi to use to control the relay, connect the `Printer Power` GPIO pin along with a single ground pin to the PSon plug on the relay board. You have to then connect the Pi's `Reset Power` GPIO pin to the `reset` pin on the relay board, leave the 5v pin next to it empty.

Then if you wish you can add a physical momentary switch to a 3rd GPIO pin & another ground pin. Then mount it somewhere of your choice on your printer. This button will act as an instant on button & re-power the printer with a single push, normally you have to manually switch both pins on yourself but now Moonraker will now activate both pins at the same time for you! Magic!

## Setup

Then you need to SSH into your pi & run:

###### NOTE: these commands are for a real Rpi, cloned system or systems built on different images will probably vary.
```
sudo nano /boot/config.txt
```
Then near the bottom of the file at the end of the first section & in the space BEFORE the start of the `[CM4]` section paste in:
```
gpio=16=op,dh # Example GPIO pin, choose a GPIO pin to control power device’s PSon pin
```
Then use the commands at the bottom of the screen to exit & save the file.

This will make sure that the GPIO pin you will use for the relay’s `PSon` pin is automatically pulled “high” when the Pi is first turned on at the beginning of the host boot sequence. This in turn should keep your relay from automatically opening & shutting the printer down while the Pi is booting. It does this at boot because the power relay is not seeing the ‘keep switched on’ signal from the Pi, & it needs that signal. 
Trust me it is very annoying if you don’t do this!

You will then need to modify your `Moonraker.conf` file by adding these…
```
[button PowerUp]
type: gpio
pin: ^gpio21 # Example GPIO pin, you can choose your own here
minimum_event_time: .05
on_press:
  {% do call_method("machine.device_power.post_device", device="Reset Power", action="on") %}
  {% do call_method("machine.device_power.post_device", device="Printer Power", action="on") %}

[power Printer Power]
type:gpio
pin:gpio16 # Example GPIO pin, you can choose your own here
on_when_job_queued: True
initial_state:on
off_when_shutdown: True
locked_while_printing: False
restart_klipper_when_powered: False
# restart_delay: 2
bound_services:

[power Reset Power]
type:gpio
pin:gpio12 # Example GPIO pin, you can choose your own here
on_when_job_queued: True
locked_while_printing: True
initial_state:off
restart_klipper_when_powered: True
restart_delay: 2
Timer:2
```
You need these two pins as the BTT relay firmware requires a reset command while the `PSon` pin is high. If this is not the case & the `PSon` pin is low (off) & you hit reset the relay power up but trip out again after 8 seconds. This is normal. The `PSon` pin must be high (on) when the reset is pressed. The PowerUp physical button will activate both GPIO pins together when pushed meaning you only need a single push of the physical button to control both pins & re-power the printer instantly.

After that add this macro to your `macros.cfg`
```
[gcode_macro M81]
gcode:
 {action_call_remote_method("set_device_power",device="Printer Power",state="off")}
```

Lastly this is used by the `PRINT_END` macro to select the Auto Shutdown feature & should be pasted into your `printer.cfg` file.
```
[output_pin PRINTER_AUTO_OFF]
pin: ### <<<<<< Insert unused board pin for state change only, monitored by system
```
This will give you full control of your power relay unit via the GUI Switch & the `PRINT_END` & `_GOODNIGHT` macros.

****************************************************************************************************************************

## Extra Bonus...
As an added bonus you can add a second physical button to a 4th GPIO pin to use as a physical Emergency Stop button!

```
[button estop]
type: gpio
pin: gpio26 # Example GPIO pin, you can choose your own here
on_press:
  {% do call_method("printer.emergency_stop") %}
```


If you made it to the end here congrats! 

I hope this macro pack makes a nice difference to your printing life, don't forget, if you feel its valuable enough to use please consider hitting that "sponsor this project" button & buying me a beer/coffee. Its always very much appreciated. Thank you & happy printing!!

[<img width="171" alt="kofi_s_tag_dark" src="https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/08473899-563b-4b4d-9409-5e6602d6ec44">](https://ko-fi.com/3dprintdemon)

# WANT MORE...??
Whats that I hear you cry, you want more?! Ok I got you covered!

How about fully automated power on/off control with auto cool down & shutdown after a print finishes?! Plus have full control even after Klipper is in shutdown! What is this black magic?!!!

Find out here!

https://github.com/3DPrintDemon/BTT-Relay-v1.2-Moonraker_INSTANT_Power-On-Button

Or maybe you're using Klicky Probe & sensorless homing & you want an AUTO E STOP system so that if your nozzle misses your endstop switch the printer knows there's a problem!

https://github.com/3DPrintDemon/Voron_2.4_AES_System_Auto_Emergency_Stop_For_Klicky_Probe

If thats not enough how about creating your very own online auto updating backup of all your config files here on Github in your own private repo?!

https://github.com/3DPrintDemon/Auto_Backup_Your_Klipper_Printer
