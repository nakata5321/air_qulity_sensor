# Air Quality Sensor

This is a prototype of indor air quality sensor. This sensor connects to Home Assistant via ESPHome.

## Requirements

list of equipment: 
- microcontroller - could be ESP32 or ESP8266 or Arduino. Tested on `esp32-c3-devkitm-1`.
- Sound Detection Sensor - HW-484/KY-037/KY-038
- Illuminance sensor - BH1750
- CO2 sensor - SCD40
- Temperature and humidity sensor - tested on SHT3X


## Run

To use this sensor you should install ESPHome tool on your PC and upload yaml file to the microcontroller. Before uploading 
configuration, open yaml file and insert your wi-fi credentials after `wifi:` key.