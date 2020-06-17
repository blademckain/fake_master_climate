# fake_master_climate

Home Assistant Fake Master Climate

Groups multiple climate devices to a single entity and create a Fake Climate that acts as a master
## How to install:

### HACS
Add this repo (https://github.com/blademckain/fake_master_climate) to the HACS store and install from there.

### local install
Put in "custom_components" folder located in hass.io inside the config folder.
(The 2 .py file must be config/custom_components/fake_master_climate)



## Sample Configuration

Put this inside configuration.yaml in config folder of hass.io

```yaml
climate:
  - platform: climate_group
    name: 'Climate Friendly Name'
    temperature_unit: C  # default to celsius, 'C' or 'F'
    entities:
    - climate.clima1
    - climate.clima2
    - climate.clima3
    - climate.heater
    - climate.termostate
	preset:
	   - name: home
	     target_temp_low
		 target_temp_high
	   - name: sleep
	     target_temp_low
		 target_temp_high
```

(use the entities you want to have in your climate_group)
