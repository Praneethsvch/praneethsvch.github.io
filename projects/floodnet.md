---
layout: page
title: FloodNet
---

## FloodNet

Remnants of Hurricanes Ida and Henri caused torrential rain and flash flooding across New York City this summer, highlighting the city’s urgent need for more resilient infrastructure.

Here below is the floods captured by the FloodNet sensors during Henri and Ida in real-time:

#### *Henri:*

 <img src="/projects/stacked_sensor_9.png" alt="a" style="zoom:25%;" />

After the Henri and Ida there is a growing interest from various agencies including [DEP](https://www1.nyc.gov/site/dep/index.page), [NOAA](https://www.noaa.gov/), [NWS](https://www.weather.gov/) and [DOT](https://www1.nyc.gov/html/dot/html/home/home.shtml) in real-time flood monitoring and alerting. According to sources from [NYCEM](https://www1.nyc.gov/site/em/index.page), flood notifications from FloodNet were received ~1hr before the first emergency alerts were reported about people stuck in vehicles at the Carroll and 4th location. The red line represents the timeline of the NYC Office of Emergency Management (NYCEM) report. 

#### *Ida:*

<img src="/projects/ida_new_stacked_sensor_4.png" alt="ida_new_stacked_sensor_4" style="zoom:25%;" />

Extreme weather events like these are expected to become more frequent as the effects of climate change become more clear and FloodNet helps target Emergency Response by monitoring floods in real time.

# Initial experiments and discovery



Initial prototyping involved evaluating the performance of different sensor technologies, including - resistive, capacitive, pressure, ultrasonic, and LiDAR, to identify an efficient solution for measuring water depth levels.



Above is an automated flood simulator that I designed during the lockdown. An MCU simulates the flood by pumping water back and forth using pumps, while the different sensor modalities record depth measurements. 

The key performance metrics tested for are - output drift, accuracy, repeatability, sensitivity, resolution, and response time. Ultrasonic sensor technology seemed to be the most reactive and accurate solution to measuring depth levels with minimal output drift over time.

<img src="/projects/lab-simulator.jpg" alt="lab-simulator" style="zoom:25%;" />

After obtaining lab access during the opening phases, I built a much cleaner flood simulator (the first one flooded my whole bedroom!).

# Sensor Development - Hardware, Firmware, and LoRaWAN protocol implementation

To incorporate LoRaWAN technology into the initial prototype, I collaborated with The Things Network developers and got my hands on feather m0 LoRa radios and programmed the initial prototype. 

<img src="/projects/components.png" alt="lab-simulator" style="zoom:24%;" />

The library used was IBM LMIC, a C based library which implements LoRaWAN-MAC in C. The examples provioded in the library were primitive and working of LoRaWAN technology requires hard real-time deadlines. After long summer battles with LMIC, I successfully developed a stable [firmware library](https://github.com/floodsense/floodsense_sensor) with ultra-low power consumption.

# Back-end development

With collaboration and supervision from my mentor [Charlie Mydlarz](https://www.cmydlarz.com/), I carried out back-end development for the following data pipeline.

<img src="/projects/data-pipeline-overview.png" alt="lab-simulator" style="zoom:25%;" />

The following is the data processing pipeline flow and methodology that I have been largely contributing to.

<img src="/projects/full-data-pipeline.png" alt="lab-simulator" style="zoom:45%;" />

# First version and deployments

After over a year of prototyping, discovery, and testing, a first version has been deployed in 6 locations within New York City.

#### *First version:*

<img src="/projects/IMG_1852.jpg" alt="IMG_1852" style="zoom:15%;" />

<img src="/projects/Image from iOS (1).jpg" alt="Image from iOS (1)" style="zoom:20%;" />

#### *Locations:*

<img src="/projects/map2.png" alt="Screen Shot 2021-06-17 at 9.50.17 PM" style="zoom:34%;" />

<img src="/projects/map1.png" alt="Screen Shot 2021-06-18 at 12.15.45 PM" style="zoom:45%;" />

# Overcoming Noise issues

Since the speed of sound is affected by temperature, humidity and other external factors, the Ultrasonic sensors are susceptible to the same factors. The noise observed in these sensors has the most correlation with the temperature. 



With a combination of statistical averaging and signal processing, this noise has been mitigated.

# Latest version and upcoming deployments

Below is the latest version of the sensor, with custom PCB and more robust sensor design. 

<img src="/projects/closeup.png" alt="Image from iOS (1)" style="zoom:40%;" />

<img src="/projects/new-breakout.png" alt="Image from iOS (1)" style="zoom:40%;" />

# QC/QAP procedures 

I devised QC/QAP protocols for sensor build process and quality control. Here is a documentation website with more information: [https://floodsense.github.io/](https://floodsense.github.io/)

