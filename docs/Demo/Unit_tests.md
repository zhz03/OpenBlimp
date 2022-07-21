# DEMO: Unit tests

## Test two esp32-cam running at the same time

 The first line are the individual tests for a single esp32 cam connecting to the router. The second line is two esp32-cam connecting to the router and running at the same time: 

 <iframe width="560" height="315" src="https://www.youtube.com/embed/ULT9MRGynQY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Configure the motor setup using input commands

 <iframe width="560" height="315" src="https://www.youtube.com/embed/C4jdIIRoYjk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## ESP32 Cam detecting green ball

 <iframe width="560" height="315" src="https://www.youtube.com/embed/f6BU70757WY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Two-way communication between two ESP32 chip

 We finished the two-way wifi communication between two esp32. 

Based on our experiment two days ago, in order to easily and quickly debug our PID paramters. We need to find a good way to tune those parameters and receive the information from the blimp for debugging purposes.  

In the following video, we have two esp32 feather boards. The left one is the master board and the right one is the slave board. We setup a two-way communication through peer-to-peer WiFi. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/FJa8eMdKWiI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

How to use this? 

(1) Debugging purpose via sending back the infomation

(2) Tunning paramters via sending the commands to the blimp

(3) Transmit ML algorithm output to the slave board

## Test live video from ESP32CAM  with ML color detection and color threshold methods 

The color threshold algorithm was tested on the live video from ESP32-cam: 

 This is the demo with low resolution: 

 <iframe width="560" height="315" src="https://www.youtube.com/embed/XkQnzLV6VKQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

 This is the demo with high resolution: 

 <iframe width="560" height="315" src="https://www.youtube.com/embed/ZHIAaimO8YY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>