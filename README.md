# homebridge-tesy-waterheater

#### Homebridge plugin to control an Tesy Water Heater

## Installation

1. Install [homebridge](https://github.com/homebridge/homebridge#installation-details)
2. Install this plugin: `npm install -g homebridge-tesy-waterheater`
3. Update your `config.json` file (See below).

## Configuration example

```json
"accessories": [
     {
       "accessory": "TesyWaterHeater",
       "name": "My Tesy Water Heater",
       "username": "mytesy_username",
       "password": "mytesy_password",
       "device_id": "XXXXXXXXXXXXXXX"
     }
]
```

### Obtaining Device Id

Login at

[My Tesy Cloud](http://mytesy.com)

with your user name and password, then open this link:

[https://www.mytesy.com/?do=get_dev](https://www.mytesy.com/?do=get_dev)

You will see a 40-character-long field named "id" - this is your device id. If you have multiple devices (Heater, Convector), config them as separate accessories.

### Structure

| Key | Description |
| --- | --- |
| `accessory` | Must be `TesyWaterHeater` |
| `name` | Name to appear in the Home app |
| `username` | Username for mytesy.com |
| `password` | Password mytesy.com |
| `device_id` | Heater (Convector) Device Id |
| `pullInterval` _(optional)_ | This property expects an interval in milliseconds in which the plugin pulls updates from your Ecoforest heater (`10000` is default)  
| `maxTemp` _(optional)_ | Upper bound for the temperature selector in the Home app (`2` is default) |
| `minTemp` _(optional)_ | Lower bound for the temperature selector in the Home app (`0` is default) |
| `model` _(optional)_ | Appears under "Model" for your accessory in the Home app |
| `serialNumber` _(optional)_ | Appears under "Serial Number" for your accessory in the Home app |

#### Bottom Line

This plugin is based on homebridge-ecoforest-heater.
