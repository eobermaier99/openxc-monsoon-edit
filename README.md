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

Future Improvements and Extensions
----------------------------------
* method to parse JSON files not copied into code but as a file
* real time connection to VIs in cars - displaying current and useful data
* accound for speed of car as a factor in how heavy rain feels on windshield of car vs actual percipitation
