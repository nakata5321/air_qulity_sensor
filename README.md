# Air Quality Sensor

This is a prototype of indor air quality sensor. This sensor connects to Home Assistant via ESPHome.

## Requirements

list of equipment: 
- microcontroller - could be ESP32 or ESP8266 or Arduino. Tested on `esp32-c3-devkitm-1`.
- Sound Detection Sensor - HW-484/KY-037/KY-038
- Illuminance sensor - BH1750
- CO2 sensor - SCD40
- Temperature and humidity sensor - tested on SHT3X

## Connection 

Most of the sensors are working over I2C. These sensors - BH1750, SCD40, SHT3X. You
should connect them over I2C bus. 
I2C bus in controller placed on:
```shell
i2c:
  sda: 18
  scl: 19
```

Sound Detection Sensor is analog sensor. You should connect it to different pin and provide it
number to configuration file. Default pin is `0`. 


## Run

To use this sensor you should install [ESPHome tool](https://esphome.io/guides/installing_esphome) on your PC and upload yaml file to the microcontroller. Before uploading 
configuration, open yaml file and insert your wi-fi credentials after `wifi:` key.

To upload firmware to controller run next:
```shell
esphome run air_quality.yaml
```

## Configuration

You can provide values for quality range for every entity. For this edit values in 46-66 lines.
