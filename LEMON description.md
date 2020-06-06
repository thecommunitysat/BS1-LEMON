Zachary Strohm
13 November 2019

# Local Environment Observation Package

## Introduction
I propose that we include a basic sensor package to monitor the local space environment around the satellite. The Local Environmental Observation Package (LEMON) is a sensor subsystem for measuring local temperature, radiation flux, illuminance, and magnetic field conditions. Measurement of temperature, Illuminance, and magnetic field can be accomplished by using small, low-power integrated circuits, while radiation will be measured with a Geiger counter, or potentially a scintillation counter. Data collected on Illuminance and the local magnetic environment can be used to determine efficiency of solar panels and tether systems respectively.

## Feasibility
There are currently many different turnkey sensor solutions available for the types of sensors above. Temperature, illuminance, and magnetic field measurement solutions can often be realized by commercially available integrated circuits. While these IC-based sensors are space and energy efficient, it can be challenging to find singular solutions for sensor systems that can operate within the environment presented in low Earth orbit. It is also important to take several factors into account while building sensor systems, including resolution, range and interface type.

## Temperature
There are many commercially available IC-based temperature sensors available on the market today. While they may seem attractive because of their space and power efficiency, IC-based sensors often have shortcomings when working in extreme environments. For space applications, operating temperature range becomes an issue. IC-based sensors typically operate from -55°C - 150°C [1], which is exceeded by the approximate temperature in LEO of -120°C to 120°C [2]. An attractive alternative is the RTD. They can measure temperatures between -200°C to 850°C [3], which is very suitable for the required range of temperatures. RTD probes can also be placed in a variety of locations on a spacecraft, and interface ICs are available for easy integration.

## Illuminance
Detecting local illuminance can be useful when determining the current energy budget of a solar-powered spacecraft. Illuminance for a solar cell (the photometric flux) can be converted to irradiance

(energy flux), by applying a conversion equation [4, a]. This enables the usage of simple photodiode- based detectors. Applications for illuminance measurements would include solar cell efficiency measurement and could also be used in ADCS if necessary.

## Magnetometry
Measuring local magnetic field conditions is useful in characterizing performance of electrodynamic tether systems. There are many commercial off the shelf sensors available, many in the form of an IC.

The most important characteristics to consider when selecting magnetometers are range, resolution, and output method. MEMS magnetometers are commonly available with selectable ranges, and can measure between +/- 16 Gauss, with a maximum resolution of approximately 0.12 milligauss [5]. Magnetic field strength in LEO is typically between 0.25 and 0.6 Gauss, so these sensors should be suitable. Magnetometer ICs are available with 3-axis measurement, along with I2C and SPI interfaces.

## Radiation
Of the measurements discussed in this document, radiation is perhaps the most difficult. The two main types of detectors are Geiger counters, and scintillation counters. Geiger tubes require a high-voltage power supply, often in excess of +500 VDC, and are constructed with potentially fragile tubes. Scintillation counters use much lower voltages but are typically very expensive. Geiger counters also cannot discriminate between types of radiation received, unlike scintillation counters. However, Geiger counters are likely the most feasible solution due to lower cost, and easier design, and have been flown on cubesat missions before. Furthermore, Geiger counter modules for cubesats exist on the market [7]. Although Geiger counters appear to be more feasible, scintillation counters should not be ruled out without further research.

## Conclusion
Flying a scientific measurement payload will increase mission impact and viability to launch providers. I provide that we include a measurement package including temperature, illuminance, magnetic field, and radiation sensors. The Local Environment Observation Package (LEMON) would be able to provide additional metrics to support primary mission goals.

## References:
[1] https://www.omega.com/en-us/resources/integrated-circuit-sensors

[2] https://www.nasa.gov/sites/default/files/files/NP-2015-03-015-JSC_Space_Environment-ISS-Mini-Book-2015-508.pdf

[3] https://sea.omega.com/sg/prodinfo/rtd.html

[4] https://www.electrical4u.com/irradiance-and-illuminance/

[5] https://www.st.com/en/mems-and-sensors/lis3mdl.html

[6] https://www.tandfonline.com/doi/pdf/10.1080/22797254.2017.1274568

[7] https://www.skyfoxlabs.com/product/16-cubesat-geiger-counter

## Appendix:
There used to be an equation here, source https://drive.google.com/file/d/1lF75NUoAwCAgLv9aP6YOIEDCOejRaAjr/view
