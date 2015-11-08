# homebridge-humidity-file

This is a plugin for [homebridge](https://github.com/nfarina/homebridge) which makes it possible to create a humidity sensor
in HomeKit via file.

## Why via file?

When you have a DHT-sensor, you need `sudo` to read from it. I don't want to run homebridge as `sudo`, so I'm having a `cronjob`, 
which writes every n seconds to a file and read from it from homebridge.

## Example config

```json
{
  "accessory": "HumidityFile",
  "name": "Humidity-sensor",
  "description": "The humidity sensor in the bedroom",
  "file_path": "/home/pi/dht/temp"
}
```
