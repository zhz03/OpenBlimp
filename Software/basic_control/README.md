# 0_Main Function of Blimp

## 1. CALIBRATION: Coupling the DC Motors, Motor Shield, and Code
### The codes, the propellers of the blimp, and the motor number in the featherboard are all coupled together -- dependent to each other. It is highly recommended that the user of this project determines the direction of each motor and list them.

### Below is how we determined the configuration for our blimp system:
### 1. Determine which motors are which:


| Direction |Motor    | Connection to Adafruit |
|------|----------------------------|-------------------------------------------|
| dir1 | Motor 1 (Vertical Left)    | Connected to Adafruit PWM Servo Driver M0 |
| dir2 | Motor 2 (Vertical Right)   | Connected to Adafruit PWM Servo Driver M1 |
| dir3 | Motor 3 (Horizontal Left)  | Connected to Adafruit PWM Servo Driver M2 |
| dir4 | Motor 4 (Horizontal Right) | Connected to Adafruit PWM Servo Driver M3 |

### 2. Test the direction of each motors 
### Based on our testing for the motors, we got the following direcions for each motor:

| Motor # (or dir in code) | Sign | Corresponding Direction | Sign | Corresponding Direction |
|--------------------------|------|-------------------------|------|-------------------------|
| dir1                     | +    | down                    | -    | up                      |
| dir2                     | +    | up                      | -    | down                    |
| dir3                     | +    | forward                 | -    | backward                |
| dir4                     | +    | backward                | -    | forward                 |


### 3. Determine the combinations of each directions that will lead to UP, DOWN, LEFT, RIGHT. Calibration or Configuration of the blimp system:
| Direction | Motor_1 | Sign_1 | Motor_2 | Sign_2 |
|-----------|---------|--------|---------|--------|
| UP        | dir1    | -      | dir2    | +      |
| DOWN      | dir1    | +      | dir2    | -      |
| FORWARD   | dir3    | +      | dir4    | -      |
| BACKWARD  | dir3    | -      | dir4    | +      |
| LEFT      | dir3    | +      | dir4    | +      |
| RIGHT     | dir3    | -      | dir4    | -      |

## 2. Libraries or Modules Used 
```
# from goal_detection.Goal_detector import Goal_detect_onBlimp
# from green_ball_detection.GB_detector import GB_detect_onBlimp
from network_code.do_connect import socket_init, get_xy_onboard, get_xy_onboard_send
import pygame
import globals
import os
from game_controller import Gcontroller
import blimp
from datetime import datetime
from data_logging import *
import blimp_control
# from green_ball_detection import GB_detector as GB_detector
import sys
from constants import *
sys.path.append("..")  # go to uppper directory
```

## 3. Logger (For Debugging Purposes)
```
logTime = datetime.now().strftime('%Y%m%d-%H%M%S')
logPath = './logs/' + logTime + '/'
if not os.path.exists('./logs/'):
    os.makedirs('./logs/')
if not os.path.exists(logPath):
    os.makedirs(logPath)
logger, formatter = logger_setup()
logger, fileHandler = fileHandler_setup(
    logger, formatter, logPath + 'logs-' + logTime + '.log')
```

## 4. Setup functions
### For greenball detection
```
def setup_GC_obj():
    """
    Set up objs
    """
    GC = Gcontroller()
    return GC
```
### For websocket connection
```
def setup_blimp_obj():
    myBlimp = blimp.Blimp(logger)
    return myBlimp
```
### For game controller or pygame
```
def setup_controller_obj():
    controller = blimp_control.blimp_control(joystick, axes)
    return controller

def setup_var():
    """
    Set up variables
    """
    system = "WIN"
    controller_id = 0
    done = False
    # control commands
    Ctl_com = [0, 0, 0, 0, "+", "+", "+", "+"]
    # flag variables
    flag = 0
    print_count = 0
    auto_init_count = 0
    bcap_man = -1
    return system, controller_id, done, Ctl_com, flag, print_count, auto_init_count, bcap_man
```

## 5. Function for killing the entire program
```
def kill_program(joystick, axes):
    if joystick.get_button(axes.get('button_LB')) and joystick.get_button(axes.get('button_RB')):
        # log_variable(logger, 'PROGRAM KILL')
        print("kill the program")
        if activate_blimp == True:
            myBlimp.serial_port_out(controller.stop_all())
        done = True
    else:
        done = False
    return done
```

## 6. Main Driver Function (inside the main function) 
### **ADD EXPLANATION HERE
```
GC = setup_GC_obj()
    GC.def_axes_val("WIN")

    if activate_blimp == True:
        myBlimp = setup_blimp_obj()
    else:
        print("Warning: blimp is not activated")

    # detector = setup_color_detector()
    system, controller_id, done, Ctl_com, flag, print_count, auto_init_count, bcap_man = setup_var()
    axes = GC.def_axes_val(system)
    if activate_cam == True:
        s, client_socket = socket_init('', SERVER_PORT)
        # s1, client_socket1 = socket_init('', SERVER_PORT1)
    else:
        print("Warning: NV cam is not activated")
```

<img src="imgs/../../../imgs/xbox_controller.png"  width="600" height="400">

###### Credits Microsoft

### **ADD EXPLANATION HERE FOR WHILE FUNCTION AND BUTTON PRESSING
```

```
### **ADD EXPLANATION HERE
```
```