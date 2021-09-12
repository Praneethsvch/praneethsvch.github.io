---
layout: page
title: FloodNet
---

## FloodNet

From prototyping in my bedroom with buckets during the lockdown to working as a core engineer collaborating with agencies, emergency response teams,  and  researchers at FloodNet, below are some key contributions.

# Initial prototyping and discovery

Initial prototyping involved performance evaluation and analysis of different sensor technologies including - resistive, capacitive, pressure, ultrasonic, and LiDAR to identify efficient solution for measuring water depth levels.

 <img src="/projects/18646.jpeg" alt="18646" style="zoom:15%;" />

Above is an automated flood simulator that I designed during the lockdown. An MCU simulates the flood by pumping water back and forth using pumps, while the different sensor modalities are logged and analyzed. Ultrasonic seemed to be the most reactive and accurate solution to measuring depth levels.



<img src="/projects/lab-simulator.jpg" alt="lab-simulator" style="zoom:25%;" />

After obtaining access to work in the lab during the opening phases, I was able to build a much cleaner flood simulator (first one flooded my whole bedroom!).

# LoRaWAN - LMIC battles

After choosing the sensor technology, the hardware team has devised a plan to incorporate LoRaWAN technology into the initital prototype. Collaborating with The Things Network, I got my hands on feather m0 LoRa radios and programmed the initial prototype. 

The library used was IBM LMIC, a C based library which implements LoRaWAN-MAC in C. The examples provioded in the library were primitive and working of LoRaWAN technology requires hard real-time deadlines. After long summer battles with LMIC, I successfully developed stable firmware with ultra-low power consumption.

# First prototype and deployment

<img src="/projects/IMG_1852.jpg" alt="IMG_1852" style="zoom:15%;" />



<img src="/projects/Image from iOS.jpg" alt="Image from iOS" style="zoom:20%;" />

<img src="/projects/Image from iOS (1).jpg" alt="Image from iOS (1)" style="zoom:20%;" />



# Dealing with Noise



# Mini version 



# Back-end development



# QC/QAP procedures 



# Design for Manufacturing (DFM)

