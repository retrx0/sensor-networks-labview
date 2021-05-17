# Smart temperature, gas and smoke detection system with LabVIEW
A simple tcp based sensor-actuator project that detects changes in temperature, increase in gas or smoke level in a house equipped with a central hub.

Smart house is a home technology which gains the information about home and communicates the information. This technology can be used to monitor and warn and carries out function conforming to elected criteria. Smart house expertise is the one awareness of the home automation ideals using set of specific set of technologies. A smart house present creative because its computer system can inform many things in our daily life. The smart house automation can interface basically using a computer interface.

Sensors data are simulated using an inbuilt sine-wave generator to get varying values at different time intervals.

## How it works
The project consist of three main parts, the [control](#control-vi) that controls all incoming data from the [sensor](#sensor-vi) and perform necessary calculations to be forwarded to the [hub](#hub-vi), the sensor that get/perceive data from the environment and finally the hub that displays the infomation to the user.

All communications are done by sending network packets over tcp.

<img src='/assets/system-chart.png' alt='system-chart' width=900 height=500 />

As can be seen below the system only works when all the system are turn on.

It is the main controller unit for all system in the house. It collects information from the house sensor and process data for the different system. It transfer control signal to house system and switching output device sensors.

<img src='/assets/system-vi.png' alt='system-chart' width=900 height=600 />

## Control VI 
The control handles all communications and decisions in the system, it decides whether it is the right time to turn on the heating or cooling also whether to turn on/off the gas and smoke detection systems and alarms base on the data it gets from the sensors.
It also house all the control systems i.e temperature, gas, and smoke systems.

<img src='/assets/control.png' alt='control vi' width=850 height=300 />

## Hub Vi
The hubs main purpose is to display the information that the control sends to it, it can also turn off/on the whole system.
It displays all the information from the control i.e which systems are on and what alarms are sounding.

<img src='/assets/hub.png' alt='hub vi' width=550 height=300 />

## Sensor VI
This VI is mainly for demsontration, it visualizes data that the sensors are perceiving from the environment, for this project all data are generated from a sine-wave generator and sent over tcp.

<img src='/assets/sensor.png' alt='sensor vi' width=500 height=300 />
