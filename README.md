
## Installation

### Scripts

tasmota_dynamic_pulse is available in [Custom-Component Repository](https://github.com/Arun-R-S/home-assistant-scripts).

Use this link to directly go to the release in Github

[Releases](https://github.com/Arun-R-S/home-assistant-scripts/releases)


### Manual

1. Download `project` from the [latest release](https://github.com/Arun-R-S/home-assistant-scripts/releases).
2. Put the files `scripts.yaml` into your `config` folder.
3. In the `configuration.yaml` file add the below line.
	  ```yaml
        script: !include  scripts.yaml
   ```
4. Now Restart the Home Assistant. The way to do that:
	- **Restart:** _Settings_ → _Developer Tools_ → _YAML_ → _Restart_. Now the configuration will check for errors and if everything is ok then a Popup will open. Select `Restart Home Assistant` option from there.
      **Note:** If you see any config error please check the configuration.yaml properly and then try restart again.
    

## Usage

With this custom script you can be able switch on the `PowerX` by updating the `PulseTimeX` value of a tasmota device through `MQTT` connection.
Note : X is the switch no. Refer the script.

1. In the script you will pass the below parameters to which will update the MQTT
- `mqtt_topic` - This is the mqtt topic where we should pass the command PulseTime with second and send the Power `on` command.
Eg:
    ```yaml
	topic: "cmnd/tasmotaDeviceNameOrTopic/PulseTime1"
	topic: "cmnd/tasmotaDeviceNameOrTopic/Power1"
    ```
- `relay_num` - This parameter refers which switch no you want to update. This number is defined in the tasmota web ui configuration
- `duration` - This parameter refere the duration of the `PulseTime` 
2. This script will pass the PulseTime then switch on the Power 




## Credits

The design is inspired by [Arun’s work][Arun-R-S].

<!-- References -->

[home-assistant]: https://www.home-assistant.io/
[home-assitant-theme-docs]: https://www.home-assistant.io/integrations/frontend/#defining-themes
[hacs]: https://hacs.xyz
[ui-lovelace-minimalist]: https://ui-lovelace-minimalist.github.io/UI/
[button-card]: https://github.com/custom-cards/button-card
[Arun-R-S]: https://arunrs.com
[release-url]: https://github.com/Arun-R-S/home-assistant-scripts/releases
