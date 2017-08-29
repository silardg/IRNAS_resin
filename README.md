# IRNAS battery pack Raspberry Pi support
This project extends the [IRNAS battery pack ](https://github.com/IRNAS/IoT-battery-pack) project with the [Raspberry Pi](https://www.raspberrypi.org/) running [resin.io](https://resin.io/).

Purpose of this project is to make the battery pack easily accessable and controllable through [resin.io](https://resin.io/).

## Supported sensors
 - ***BQ2429***
 - ***MAX1720***

## Main files

#### BQ2429x.py
Python script for connecting to the BQ2429 chip and interfacing with it.

```__init__()``` - connects to the device through the I2C module

```get_status(type_of_status)``` - reads out the ***status*** register and returning data dependent on the ***type_of_status*** parameter

```get_faults(type_of_fault)``` - reads out the ***faults*** register and returning data dependent on the ***type_of_fault*** parameter

```set_ter_prech_current(termination, precharge)``` - writes data to the ***term/prech*** register

```set_charge_voltage(c_v_l, precharge, thresh)``` - writes the data to the ***voltage charge*** register

#### MAX1720.py
Python script for connecting to the MAX1720 chip and interfacing with it.

```__init__()``` - conects to the device through the I2C module

```get_cell_voltage()``` -  gets the lowest cell voltage

```get_max_voltage()``` - gets the max voltage the cell was on since reset

```get_current()``` - get the current running from the cells

```get_avg_current()``` - get the average current consumption

```get_maxmin_current()``` - get the max and minimum current since reset

```get_temperature()``` - get the current temperature

```get_SOC()``` - get a percentage of the capacity

```get_capacity()``` - get the capacity

```get_TTE()``` - get the estimated time to empty

```get_TTF()``` - get the estimate time to full

```get_battery_status()``` - checks if the battery is absent or not

```reset_minmax_current()``` - reset the minmax values (sets the minmax register to default)

```set_average_current_update_time(value)``` - sets the average current monitoring time

---

#### License

All our projects are as usefully open-source as possible.

Hardware including documentation is licensed under [CERN OHL v.1.2. license](http://www.ohwr.org/licenses/cern-ohl/v1.2)

Firmware and software originating from the project is licensed under [GNU GENERAL PUBLIC LICENSE v3](http://www.gnu.org/licenses/gpl-3.0.en.html).

Open data generated by our projects is licensed under [CC0](https://creativecommons.org/publicdomain/zero/1.0/legalcode).

All our websites and additional documentation are licensed under [Creative Commons Attribution-ShareAlike 4 .0 Unported License] (https://creativecommons.org/licenses/by-sa/4.0/legalcode).

What this means is that you can use hardware, firmware, software and documentation without paying a royalty and knowing that you'll be able to use your version forever. You are also free to make changes but if you share these changes then you have to do so on the same conditions that you enjoy.

Koruza, GoodEnoughCNC and IRNAS are all names and marks of Institut IRNAS Rače. 
You may use these names and terms only to attribute the appropriate entity as required by the Open Licences referred to above. You may not use them in any other way and in particular you may not use them to imply endorsement or authorization of any hardware that you design, make or sell.

