---
layout: page
title: FloodNet
---

## FloodNet

From prototyping in my bedroom during the lockdown to working as a core engineer, below are contributions to the entire sensor development cycle at FloodNet.

# Initial experiments and discovery



Initial prototyping involved evaluating the performance of different sensor technologies, including - resistive, capacitive, pressure, ultrasonic, and LiDAR, to identify an efficient solution for measuring water depth levels.

 <img src="/projects/18646.jpeg" alt="18646" style="zoom:15%;" />

Above is an automated flood simulator that I designed during the lockdown. An MCU simulates the flood by pumping water back and forth using pumps, while the different sensor modalities record depth measurements. 

The key performance metrics tested for are - output drift, accuracy, repeatability, sensitivity, resolution, and response time. Ultrasonic sensor technology seemed to be the most reactive and accurate solution to measuring depth levels with minimal output drift over time.

<img src="/projects/lab-simulator.jpg" alt="lab-simulator" style="zoom:25%;" />

After obtaining lab access during the opening phases, I built a much cleaner flood simulator (the first one flooded my whole bedroom!).

# LoRaWAN battles

After choosing the sensor technology, the [hardware team](https://www.floodnet.nyc/partners/) has devised a plan to incorporate LoRaWAN technology into the initital prototype. Collaborating with The Things Network, I got my hands on feather m0 LoRa radios and programmed the initial prototype. 

<img src="/projects/components.png" alt="lab-simulator" style="zoom:24%;" />

The library used was IBM LMIC, a C based library which implements LoRaWAN-MAC in C. The examples provioded in the library were primitive and working of LoRaWAN technology requires hard real-time deadlines. After long summer battles with LMIC, I successfully developed stable firmware with ultra-low power consumption.

# Back-end development

<img src="/projects/data-pipeline-overview.png" alt="lab-simulator" style="zoom:25%;" />

<img src="/projects/full-data-pipeline.png" alt="lab-simulator" style="zoom:45%;" />

# First version and deployments

<img src="/projects/IMG_1852.jpg" alt="IMG_1852" style="zoom:15%;" />

<img src="/projects/map2.png" alt="Screen Shot 2021-06-17 at 9.50.17 PM" style="zoom:34%;" />

<img src="/projects/map1.png" alt="Screen Shot 2021-06-18 at 12.15.45 PM" style="zoom:45%;" />



<img src="/projects/Image from iOS.jpg" alt="Image from iOS" style="zoom:20%;" />

<img src="/projects/Image from iOS (1).jpg" alt="Image from iOS (1)" style="zoom:20%;" />





# Dealing with Noise




# Floods captured during Henri and Ida

<img src="/projects/henri_new_stacked_sensor_4.png" alt="henri_new_stacked_sensor_4" style="zoom:25%;" />

<img src="/projects/ida_new_stacked_sensor_4.png" alt="ida_new_stacked_sensor_4" style="zoom:25%;" />

# Latest version and upcoming deployments

<img src="/projects/closeup.png" alt="Image from iOS (1)" style="zoom:40%;" />

# QC/QAP procedures 



# Design for Manufacturing (DFM) and Growth of FloodNet

