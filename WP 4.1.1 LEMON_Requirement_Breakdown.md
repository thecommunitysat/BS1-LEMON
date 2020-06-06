# LEMON Requirement Breakdown
Part of WP 4.1.1 LEMON Sensor choice
The LEMON package consists of sensors that measure the following quantities: temperature, luminous flux, radiation and magnetic flux density.

*All values are target values and are subject to further change depending on part availability and system robustness


## Temperature Measurement System (TMS)
The TMS will consist of two sensors, one for measuring the internal temperature of the spacecraft, and one measuring the external.

. | Desc. | Value | Notes
--|--|--|--
TMS.1 | Temperature Range | -25°C - +80°C Internal, -85°C - +100°C External | 
TMS.2 | Resolution | 0.045 °C | Ext. Range/4096 (for a 12-bit system with maximum range of -85°C-100°C)
TMS.3 | Bit Depth | 12 Bit | 
TMS.4 | Accuracy | ±0.5 °C | Somewhat arbitrary value well within the range of PTD capabilities.
TMS.5 | Channels | 2 | 
TMS.6 | Measurement Size | 24b (3B) | 2*12-bit
TMS.7 | Data Rate | 6B/min ** | 1  meas. per 30 sec.

**1B = 8b (Assuming an 8-bit MCU for these calculations and requirements, and measuring twice per minute)


## Luminous Flux
There will be 6 luminous flux sensors (one for each face that has a solar panel).

. | Desc. | Value | Notes
--|--|--|--
LUM.1 | Range | 0-1500 W/m2 | 
LUM.2 | Resolution | 0.37 W/m2 | Range/4096
LUM.3 | Bit Depth | 12 Bit | 
LUM.4 | Accuracy | ±0.5 W/m2 | Might be unreasonable
LUM.5 | Channels | 6 | # of Channels
LUM.6 | Measurement Size | 72b (9B) | 6*12 bit
LUM.7 | Data Rate | 18B/min | 1 meas. Per 30 sec.


## Radiation

. | Desc. | Value | Notes
--|--|--|--
RAD.1 | Range | 4-40 krad/yr | 
RAD.2 | Resolution | 10 rad | Depends on type
RAD.3 | Channels | 1 | 

*** Appropriate radiation values depend on technology used assuming a RADFET, radiation is measured in rad/time or gy/time, still working on final details.


## Magnetometry

. | Desc. | Value | Notes
--|--|--|--
MAG.1 | Range | 30μT-60μT | 
MAG.2 | Resolution | 7nT | Range/4096
MAG.3 | Bit Depth | 12 bit | 
MAG.4 | Accuracy | ±1nT | A resolution of 7nT results in an accuracy of at best ±3.5nT
MAG.5 | Channels | 1 | 
MAG.6 | Measurement Size | 12b (1.5B) | 12 bit
MAG.7 | Data Rate | 3 B/min | 1 meas. Per 30 sec.


