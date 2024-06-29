# Demon_Klipper_Essentials_Unified
The very latest UNIFIED version for these macros! Huge re-implementation &amp; new Features!

[<img width="171" alt="kofi_s_tag_dark" src="https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified/assets/122202359/08473899-563b-4b4d-9409-5e6602d6ec44">](https://ko-fi.com/3dprintdemon)

### Made to make your printing life easier & your printer SMARTER!
### I hope you enjoy these automatic & highly adaptive macros! Don't forget if you like & use this project you can buy me a beer/coffee to say thanks. https://ko-fi.com/3dprintdemon
A lot of time, testing, love & coffee has been poured into them!
If you feel you’d like to support my efforts & help to enable me to continue sharing my ideas please consider buying me a beer/coffee at the provided “Sponsor this project” link. Thanks!

# WELCOME TO 3DPrintDemon DEVILISHLY GOOD Klipper macros!

# This UNIFIED version will run on almost any COREXY or BED SLINGER (cartesian) Klipper printer with no changes needed to the macro files! 
Small user setting changes will be required of course.

The macros will check what machine you have & adapt themselves to it automatically! So for example if you hit `GANTRY_LEVEL` on a COREXY printer you'll get a `QUAD_GANTRY_LEVEL`, but if you do the same on a bed slinger you'll get a `Z_TILT_ADJUST` - IF your printer has that feature enabled! Same macro button but different function! Also there is a built in smart park, where the printer knows if you have a probe based Z endstop or a switch & will adjust the parking height during macro events to suit your system! Further hardware options are manually selectable in the user settings file.

Checks & Error Handling. This is a big problem for many users, you get an error in klipper but its written in "code" so you cant tell what it means! Here I have tried to explain all errors that occur while running the macros clearly. Sadly I cant help the "encoded" system ones! They'll still be hard to read!

# These macros rely on you setting the correct filament type in your slicer! BE SURE YOU DO THIS!

### NOTE: This version is a totally new approach to these macros & therefore have only been tested on my machines, while every effort has been made to make sure they work well there could well be a few bugs that need squashing! So please be sure to report anything that doesn't work correctly or errors you come across. However if you're able please try to solve the issue yourself first & let me know your solution so I can merge it. Thanks all!

# FEATURES:

### NEW! ORCA Slicer `Multi_Surface` handling! 
- The printer knows what bed surface you choose to use & can add a pre-set Z offset for the print & remove it afterward! The system can even combine the surface offset with a filament or temperature based one! Don't worry though there are `Bed Saver` safety checks that should help stop you entering a wrong number & damaging your printer, especially when using the combine offset function!

### NEW! Random nozzle cleaning movements! 
- No more single path cleaning to wear out your brush/pad! All movements are randomly generated!

### NEW! Random filament purge parking! 
- No more purging in the same spot over & over piling filament on top of filament!

### NEW! Now includes the Demon Bed Fans Monitor!
- NEW! Now with Floating fan chamber control! The system will raise or low fan speed depending on temperature!
- Smart & fully adaptive Bed Fans control system!
- Full instructions available here in the `bed_fans.cfg` file

### NEW! The Demon AES System! 
- Save your printer from damage from homing errors when using a Z Endstop switch & Sensorless homing! This could save you a lot of money if homing fails!
- Full instructions available here: https://github.com/3DPrintDemon/Voron_2.4_AES_System_Auto_Emergency_Stop_For_Z_Endstop_Switch

### NEW! Start Macro handling for Smart Filament Sensor Encoder
- Disables the sensor until the macro completes

### NEW! Support for Klipper's `ADAPTIVE_MESH` system in the latest Klipper update
- NOTE you need the latest version of Klipper to use this!
-  If you own a Sovol SV06/Plus with a Sovol Klipper screen or a Sovol SV07/Plus & want to use the latest version of Klipper with Adaptive Meshing & more features you need to follow my How2 guide on how to update the Sovol Klipper screens on your printers.

https://github.com/3DPrintDemon/How-to-Update-Sovol-Klipper-Screen-To-Latest-Klipper-SV06-and-SV07 

### NEW! Adaptive Pressure Advance Mode! - APA - ORCA SLICER ONLY

- Why have only 1 single setting for Pressure Advance trying to work across the whole print when you can have 6!!

- 6 settings per filament, 30 in total!

- Each setting is automatically selected by filament for different types of extrusions during the print.

- Settings for Perimeter, External Perimeter, Internal Infill, Solid Infill, Top Solid Infill, & filament default.

- Print tuning towers for the speed of each extrusion type & apply them to the Adaptive Pressure Advance (APA) modifiers!

- Disable or enable individual modifiers, you don't have use them all, use any number in any combination!

- Or disable modifiers by filament or the whole module at once!

- All settings in one easy to edit place, no need to edit macro code!

- Verbose mode, read back all APA commands to the console!

### These macros rely on you setting the correct filament type in your slicer! BE SURE YOU DO THIS!

### Mesh Auto Builder!

- Auto build all 5 meshes at different temperatures with included heat soak waits & message prompts! Inspired by a community contribution from Karl L! Thank you for sharing!


### **Demon Print Start End**

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

- Customise your purge line! Choose where to start & which axis to purge along! X or Y! It automatically adapts to your file's extrusion height & width!



### **Demon User Settings**

- This file contains all the 'Variables' available for the Demon Print Start End Macro, open & edit one single file! No need to trawl through the macros!

- You can even turn on/off hardware options as your system changes & grows over time! Don't worry about future-proofing, its already built right in!



## Included User executable macros:

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




## Introduction

These macros are smart & have adaptive properties & will shape themselves to what you’re printing. 
For example the macros know if your printer is CoreXY or bed slinger, they know if it's already homed so wont home it again, & can not only automatically shape itself to simple things like your printer’s bed size & what temperatures you’re printing at, but it will even know the current file’s first layer height so it’ll print the purge lines at the same height! Plus it can automatically choose & load the correct mesh for the temperature of your print, as your bed will slightly change shape the hotter it gets. 

Not only that but it will choose the correct settings for your chamber cooling system, & it will even check to see if you have filament loaded before starting a print! …We’ve all done that one haven’t we, be honest!!

Also it can decide if your chamber needs to be heat soaked or not before the print starts! This is fantastic for saving time, money & electricity between back-to-back prints where the system doesn’t require heat soaking as it’s already up to temperature!! 

You have all this plus step by step adaptive on screen messages on any Mainsail web interface & KlipperScreen system so you know exactly what your machine is deciding to do at any time! Some macros can be customised by changing the settings in the macro button options before you manually call the macro in the Mainsail or KlipperScreen interfaces!

It doesn't end there, as all these features are user customisable within the Macro Variables sections inside the files! Some functions can be totally deactivated entirely & bypassed with a simple changing an option from `True` to `False`! This is very useful if your printer doesn’t have the hardware components installed at this time but leaves the configuration easily customisable with a few keystrokes in the future if you want to add to your machine!

With the `_GOODNIGHT` macro you can even flick a GUI switch in Mainsail to let the printer know you want it to auto power down after it’s finished printing!! 
This can be done at ANY point during the print! You can even change your mind & cancel the auto shutdown at any point before the print completes!

**NOTE: Additional hardware & setup is required for this feature to work! How to do this is explained further on in this readme file.**

The `_RET_CALI_START` macro is used when calibrating your retraction settings with files generated at:

http://www.retractioncalibration.com/

All you need do is paste `_RET_CALI_START` into the website's "Custom Gcode" box next to the green "Generate Gcode" button
This is without a doubt the absolute BEST retraction test out there!

The `CLEAN_NOZZLE`, `LOAD_CLEAN`, & `UNLOAD_CLEAN` macros are for use with a nozzle cleaning brush found here:

For VORON 2.4 printers
https://www.printables.com/model/201999-nozzle-scrubber-with-a-little-bucket-for-voron-24

For SV08 Printers
https://www.printables.com/model/873006-sovol-sv08-silicone-nozzle-cleaner-purge-bucket-mi
 

## All sounds great right!? Ok well here’s the tricky bit! 
…Well its not that tricky because I got it all written down here for you to just copy/paste into your setup!

### FOR ANY FILE SPECIFIC INSTRUCTIONS & VARIABLES PLEASE CHECK THE FILE TEXT!

**Don’t just install & run them & wonder why they don’t work! They WILL need setting up once on your system. Damage to your machine may result if the macros are run without the prerequisites or without the correct setup before first use!** 

You will need to add some lines to your slicer's `Start G-code` & `End G-code` boxes to get the `PRINT_START` macro to work correctly. 

These are in the `demon_print_start_end.cfg` file.

# Prerequisites
You must download & `[include]` these two additional files along with these Demon Macros or they will NOT work correctly.

These additional macros are prerequisites:

For VORON PRINTERS
- https://github.com/rkolbi/voron2.4/blob/main/non-blocking_wait.md
- https://github.com/VoronDesign/Voron-Stealthburner/blob/main/Firmware/stealthburner_leds.cfg 

For SOVOL SV08 PRINTERS & OTHER MACHINES
- https://github.com/3DPrintDemon/Non_Blocking_Wait_Sovol/releases/tag/Heat_Soak_Timers_V1.0
- https://github.com/3DPrintDemon/Voron-Stealthburner/blob/main/Firmware/RGB_LEDs.cfg


The rest of the macros are simple single click automations for running a series of tasks you’d normally have to remember the correct procedure for & are a hassle to run multiple times if done manually. They’re quality of life macros to help you get the best setup & results from your printer. 

# BE SURE TO SET YOUR MACRO VARIABLES  

- `_CLEAN_VARIABLES` the printer will give you an error if you haven’t done this & try to use the macros.

Long video on settings walkthrough: https://youtu.be/s4poVSt5a2g


****************************************************************************************************************************
# IF YOU RAN V1.0-V2.6 BE SURE TO UPDATE YOUR SLICER'S START GCODE AS PER V2.7 FILE OR NEW FEATURES WONT WORK!
# Instructions to do this are in the files.
# Also you must update ALL the macro files as this new version will NOT work correctly with old files!
****************************************************************************************************************************

* If you own a Sovol SV06/Plus with a Sovol Klipper screen or a Sovol SV07/Plus & want to use the latest version of Klipper with Adaptive Meshing & more features you need to follow my How2 guide on how to update the Sovol Klipper screens on your printers.

https://github.com/3DPrintDemon/How-to-Update-Sovol-Klipper-Screen-To-Latest-Klipper-SV06-and-SV07 

# INSTALL

Copy the files here into a folder called `Demon_Klipper_Essentials_Unified` in your config folder on your printer. 

NOTE: If you download the zip file via the button at the top of the repo your downloaded folder will be called:
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

# This is easier!
Or you can SSH into your system & use...

```
cd /home/pi/printer_data/config
```
NOTE: the above command is for a real Raspberry Pi, if you're using a cloned system that "/pi" folder will change to `mks` or `btt` or `sovol` or similar.

```
git clone https://github.com/3DPrintDemon/Demon_Klipper_Essentials_Unified.git
```

Then, paste into your printer.cfg
```
[include ./Demon_Klipper_Essentials_Unified/*.cfg]
```

This will bring these files into your system, be sure to comment out & NOT delete your current START & END PRINT Macros just yet!

Lastly in Mainsail click the cogs top right of the screen & then click the `RESTORE` button in the `Interface Settings` window & find the `backup-mainsail-DEMON-MACROS.json` file to bring in the macro setup.


## You should also be sure to `[include mainsail.cfg]` as we will be using this!

You need to open the `Mainsail.cfg` file & copy out the `[gcode_macro _CLIENT_VARIABLE]` & place it all into an editable macros.cfg file, as that `Mainsail.cfg` is read only.

Then setup the park positions are you want or need them.

Now were it says `variable_user_pause_macro : ""` you need to paste in...
```
_Z_RAISE
```
Between the quote marks so it looks like this: `"_Z_RAISE"`


Now do the same for `variable_user_cancel_macro: ""`


# Additional Configuration

## Auto Shutdown Moonraker Power Device

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

NOTE: these commands are for a real Rpi, cloned system or systems built on different images will probably vary.
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

## Chamber Monitoring & Fan Control

To get the most from these macros you’ll need to add a Chamber thermistor to your machine if you haven’t already & a Chamber exhaust fan. 
- If you have a Chamber exhaust fan call it `[temperature_fan chamber]`
- If you instead have a Chamber Thermistor only & no Exhaust fan call it `[temperature_sensor Chamber_Temp]`

## Printer LED lights
- If you have printer LED lights (NOT neopixel) call them `[output_pin Printer_Lights]`
- NeoPixel LED's are dealt with in the additionally installed files.

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
 pause_on_runout: True
 insert_gcode:
     { action_respond_info("Filament Encoder is Running") }
 runout_gcode:
     { action_respond_info("Filament Encoder Stall Detected") }

 [delayed_gcode encoder_sensor]
 initial_duration: 1
 gcode:
    SET_FILAMENT_SENSOR SENSOR=encoder_sensor ENABLE=0
```

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

[menu __main custom return]
name: Return Toolhead
icon: bed-level-b-l
method: printer.gcode.script
params: {"script":"return_toolhead"}

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

## Extra Bonus...
As an added bonus you can add a second physical button to a 4th GPIO pin to use as a physical Emergency Stop button!

```
[button estop]
type: gpio
pin: gpio26 # Example GPIO pin, you can choose your own here
on_press:
  {% do call_method("printer.emergency_stop") %}
```

## Updated to include the new integrated KLIPPER Adaptive Mesh option. There is no longer any need for a separate KAMP install.

For the Adaptive Mesh feature to work you must have:
- The latest version of Klipper!*
- Enabled your Slicer for `Exclude Objects`
- Added the `Exclude Objects` section to your `moonraker.conf` file
- Added the `Exclude Objects` section to your `printer.cfg` file

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

## To use adaptive meshing all files MUST have been sliced with `Exclude Objects` active.
## IF NOT YOU WILL RECEIVE THE FOLLOWING ERRORS!!

If you use ORCA SLICER:

`Error evaluating 'gcode_macro PRINT_START:gcode': gcode.CommandError: This error is caused by the sliced file not having EXCLUDE_OBJECT enabled! Please disable Adaptive_Meshing in the user_settings.cfg or re-slice the file with it enabled and restart the print!`

If you use another slicer:

`Internal error on command:"PRINT_START"`

`Internal error on command:"BED_MESH_CALIBRATE"`


## Fin...
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
