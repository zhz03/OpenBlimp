# Build Your System Hardware

In this chapter, we will talk about system hardware in details, the overall system hardware consists following part as shown in the picture: 

![](https://raw.githubusercontent.com/zhz03/OpenBlimp/develop/Hardware/Images/assembly/design_framework.jpg)

Let's talk about the most critical part first: Electronics system.

Electronics system is very important to a blimp. The blimp electronics system oftentimes is consist of following parts as shown below:

- Control board
- Motor diver
- Motors + propellers
- Li-po Battery
- Other sensors (like Camera, lidar sensors, ultrasonic sensors). Sensor are not necessary for you blimp, it really depends on your needs. 

As other parts of your blimp, you may also need:

- Payloads: 

  This is to help balancing your blimp if $F_B > m_{total}$

- Fins and other surface: 

  This is for stabilize your blimp. We will not go into the details here, there are so many aerodynamics knowledge. 

Next, I will talk about each part of these in order to help you understand why your blimp electronics system needs to connect this way and how do they work as a whole team.

## Control board

Control board is like the brain of your blimp, it process data, calculate things, distribute powers and send all your commands to different parts.

We explored several control board solutions, all of these controllers should satisfy:

- Light enough to put it on your blimp
- Able to process the basic control commands 
- Has communication devices on it
- Enough pinout for wire connection

Our control board include: 

- NodeMCU ESP8266
- Raspberry Pi zero W
- NodeMCU ESP32
- Featherboard ESP32

## Motor driver

Motor driver is to control and power your motors. We also explored three different motor driver:

- tb6612
- pololu driver board
- Featherboard motor shield



## Motors + propellers

Motors propellers the power source to let you manipulate your blimp.

We have explored two different types of motors:

- DC motors 
- Brushless motors

As for the propellers, we also explored different size of propellers, as long as they are compatible with your motors, then it should be enough.

As for brushless motors, you also need esc to power it. 

## Electronics Assembly

There are different types of electronics combinations:

- NodeMCU ESP8266 + tb6612 * 2 + DC motor propellers
- ​

Here is one example of wiring all electronics together:

![](https://raw.githubusercontent.com/zhz03/OpenBlimp/develop/Hardware/circuit_plot_doc/manualCtl_NodeMCU.png)

## Overall Assembly

[Feather board ESP32 assembly](https://learn.adafruit.com/adafruit-huzzah32-esp32-feather/assembly)