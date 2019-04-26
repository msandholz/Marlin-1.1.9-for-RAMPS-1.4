# Marlin-1.1.9-for-RAMPS-1.4
Compile Marlin 1.1.9 for RAMPS 1.4 / Arduino mega2560 / Graphic Controler 12864

# Documentation
Documentation can be found here:
- Marlin Homepage [http://www.marlinfw.org] 
- Umbau auf RAMPS [https://chinadrucker.de/2017/3d-drucker-aufbau-umbau-auf-ramps-1-4-am-beispiel-anet-a8-inkl-marlin-installation/]

# Components
Used Components:
- RAMPS 1.4 Board
- Arduino-Mega 2560
- Reprap Discount 12864 LCD – full Graphic Display with SD-Cardreader
- Stepperdriver Type A4988 (16 Steps)

# Installation

1. Set Jumper for Stepperdriver (no no yes | 1/16 step)
2. Load Marlin Firmware under [http://marlinfw.org/docs/basics/install.html#download]
3. Edit `Configuration.h` and change the following lines
   ```
   126 | #define BAUDRATE 115200
   ```
   
   ```
   133 | #ifndef MOTHERBOARD
   134 |    #define MOTHERBOARD BOARD_RAMPS_14_EFB
   135 | #endif
   ```
   
   ```
   139 | #define CUSTOM_MACHINE_NAME "Sandholz Engineering"
   ```
   
   ```
   149 | #define EXTRUDERS 1
   ```
   
   ```
   152 | #define DEFAULT_NOMINAL_FILAMENT_DIA 1.75
   ```
  
   ```
   313 | #define TEMP_SENSOR_1 0
   314 | #define TEMP_SENSOR_2 0
   315 | #define TEMP_SENSOR_3 0
   316 | #define TEMP_SENSOR_4 0
   317 | #define TEMP_SENSOR_BED 1
   318 | #define TEMP_SENSOR_CHAMBER 0
   ```
   
   ```
   416 | #define PIDTEMPBED
   ```
   
   ```
   611 | #define DEFAULT_AXIS_STEPS_PER_UNIT   { 100, 100, 400, 95 }
   ```
