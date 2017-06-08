# OpenXC Monsoon Edit
OpenXC application to map data from windshield wipers based off Bug Labs freeboard monsoon application

Differences from BugLabs' Freeboard Emulator
--------------------------------------------
focus is on mapping data, rather than other freeboard data displays
* non-boolean data, and thus able to map density
* more data points at one time
  * over 1,000 data points in heatmap array generated from JSON objects
* no time dependent animation
* JSON files copied into html file rather than accessed

VI Firmware
-----------
The firmware used to take the more detailed wiper data was written over previous wiper data firmware. 
This version of firmware returns the wiper state string for newer cars with detailed status. 
Any cars without the detailed status will return boolean data.

Editing Trace Files
-------------------
Trace files should be validated, stripped, and normalized in python, the same way the BugLabs freeboard monsoon files were.
https://github.com/emarsman/openxc-buglabs/blob/master/scripts/README.md

HTML FILE
---------
Edited trace files must be copied in as strings as of right now. 
Currently, two trace files should be there, and it should look like this: 
![Map](https://github.com/eobermaier99/openxc-monsoon-edit/blob/master/Mapped%20Data.PNG)

In order to change map/display appearances, follow Google Maps API documentation for JavaScript:
https://developers.google.com/maps/documentation/javascript/adding-a-google-map

Possible Future Improvements and Extensions
----------------------------------
* method to parse JSON files not copied into code but as a file
  * see code with single trace to see different failed attempts to retrive data commented out
  * note that the url being accessed no longer exists, but was simply a validated, stripped, normalized trace file
* real time connection to VIs in cars - displaying current and useful data
* account for speed of car as a factor in how heavy rain feels on windshield of car vs actual percipitation
