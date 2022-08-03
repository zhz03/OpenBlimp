

# Capability extension

## Shape extension

For users who wants to develop your own shape of blimps, you need to make different 2D shapes for DIY Mylar Envelope. Here, we provide some ideas of how to make different balloon shape:

![2d > 3d transform]()

## Sensing module extension

### Camera

Visual sensing if the main sensing method in our OpenBlimp framework. We have explored lots of embedded cameras modules like  [FPV Cam](),[ESP32 Cam](), [OpenMV Cam](), [Esp EYE](),[Neloca Cam](). 

Since we provide different type of cameras, it would be great to pick the camera based on users needs. However, escept for the FPV cam, all the other cameras requires to upload a program to its on-board-chip before using these cameras. 

### Lidar

Lidar is also a very useful distance sensor for blimp. By using control board we provided, Lidar sensor can easily be extended to our current setup. The Lidar sensor that we use is [hsd]() 

### Ultrasonic 

Ultrasonic sensor is another distance sensor for blimp. 

## Control module extension

## Manual control

### Code structure

```bash
├───base_station
│   ├───ball_detection
│   │   ├───distance-detection-torch
│   │   └───model_weights
│   ├───logs
│   └───pid
└───feather_board
```

## Autonomous control



