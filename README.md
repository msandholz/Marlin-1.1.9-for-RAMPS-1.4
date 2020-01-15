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
- Stepperdriver Type TMC2208 v1.1

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
   139 | #define CUSTOM_MACHINE_NAME " Sandholz Engineering"
   ```
   
   ```
   149 | #define EXTRUDERS 1
   ```
   
   ```
   152 | #define DEFAULT_NOMINAL_FILAMENT_DIA 1.75
   ```
  
   ```
   313 | #define TEMP_SENSOR_0 1
   314 | #define TEMP_SENSOR_1 0
   315 | #define TEMP_SENSOR_2 0
   316 | #define TEMP_SENSOR_3 0
   317 | #define TEMP_SENSOR_4 0
   318 | #define TEMP_SENSOR_BED 1
   319 | #define TEMP_SENSOR_CHAMBER 0
   ```
   
   ```
   416 | #define PIDTEMPBED
   ```
   
   ```
   530 | // Mechanical endstop with COM to ground and NC to Signal uses "false" here (most common setup).
   531 | #define X_MIN_ENDSTOP_INVERTING true // set to true to invert the logic of the endstop.
   532 | #define Y_MIN_ENDSTOP_INVERTING true // set to true to invert the logic of the endstop.
   533 | #define Z_MIN_ENDSTOP_INVERTING true // set to true to invert the logic of the endstop.
   ```
   
   ```
   553 | #define X_DRIVER_TYPE  TMC2208_STANDALONE
   554 | #define Y_DRIVER_TYPE  TMC2208_STANDALONE
   555 | #define Z_DRIVER_TYPE  TMC2208_STANDALONE
   559 | #define E0_DRIVER_TYPE TMC2208_STANDALONE
   560 | #define E1_DRIVER_TYPE TMC2208_STANDALONE
   ```

   ```
   611 | #define DEFAULT_AXIS_STEPS_PER_UNIT   { 100, 100, 400, 95 }
   ```

   ```
   619 | #define DEFAULT_MAX_FEEDRATE          { 250, 250, 8, 25 }
   ```
   
   ```
   648 | #define DEFAULT_XJERK                  5.0
   649 | #define DEFAULT_YJERK                  5.0
   650 | #define DEFAULT_ZJERK                  0.4
   651 | #define DEFAULT_EJERK                  5.0
   ```

   ```
   1226 | #define EEPROM_SETTINGS // Enable for M500 and M501 commands
   ```

   ```
   1257 | // Preheat Constants
   1258 | #define PREHEAT_1_TEMP_HOTEND 190
   1259 | #define PREHEAT_1_TEMP_BED     60
   1260 | #define PREHEAT_1_FAN_SPEED     0 // Value from 0 to 255
   1261 | 
   1262 | #define PREHEAT_2_TEMP_HOTEND 235
   1263 | #define PREHEAT_2_TEMP_BED     80
   1264 | #define PREHEAT_2_FAN_SPEED     0 // Value from 0 to 255
   ```
   
   ```
   1509 | #define SPEAKER
   
   1518 | #define LCD_FEEDBACK_FREQUENCY_DURATION_MS 2
   1519 | #define LCD_FEEDBACK_FREQUENCY_HZ 1000
   
   ```
   


   ```
   1429 | #define SDSUPPORT
   ```
   
   ```
   1659 | #define REPRAP_DISCOUNT_FULL_GRAPHIC_SMART_CONTROLLER
   ```
  
  4. Enable `Manual Bed Leveling` and `Mesh Bed Leveling`
  
   ```
   980 | #define MESH_BED_LEVELING
   986 | #define RESTORE_LEVELING_AFTER_G28
   1102| #define LCD_BED_LEVELING
   
   ```
  
  5. Load `U8glib` and copy it into the `library-folder` of the Arduino IDE.
   
  6. Option: Dual Extruder (2in1)
  
   ```
   149 | #define EXTRUDERS 2
   155 | #define SINGLENOZZLE
   ```
   
   6. Option: Dual Extruder (2in2)
  
   ```
   149 | #define EXTRUDERS 2
   
   306 | #define TEMP_SENSOR_0 1
   307 | #define TEMP_SENSOR_1 1
   ```
   
   
  7. Compile Files and upload it to Arduino-Mega 2560 - Board
  
  
   
