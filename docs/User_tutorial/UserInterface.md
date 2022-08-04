

# User interface

## Introduction

We provided several user interface in OpenBlimp to satisfy different needs. Our user interface includes:

- **Blynk App**

  Our user interface is using Blynk app for any users who have cellphone to download.

  *Blynk* platform powers low-batch manufacturers of smart home products, complex HVAC systems, agricultural equipment, and everyone in between.

- **Game Controller**

  Game controller provides lots of physical joystick and buttons which is good for controlling without seeing. The physical feedback from joystick will help in better control. **Therefore, this method is most recommended.**

- **Keyboard**

  For those who doesn't want to use Game controller and Blynk App, keyboard is also another available option that we provide. 

## Blynk App 

### Installation

To download Blynk mobile app, please check their [website](https://docs.blynk.io/en/downloads/blynk-apps-for-ios-and-android)

![blynk_apps](https://raw.githubusercontent.com/zhz03/OpenBlimp/develop/imgs/blynk_apps.png)

### Control interface

Our recommended Blynk interface is shown as below:

![](https://raw.githubusercontent.com/zhz03/OpenBlimp/develop/imgs/interface.jpg?resize==50)

You can also customize your own interface as long as you have the following functionality:

- **Control panel**: your control panel should include two joystick and one slider to give you the ability to control motion primitives(horizontal, vertical and rotation) and all motor propellers speed.
- **Configuration commands**: this will be the *terminal* widgets in the Blynk. This is for sending to correct configuration commands to configure the hardware mapping.


### Usage



## Game Controller 

### Installation

Git clone the repository:

Navigate to the following directory:

### Control interface

The illustration figure of game controller is shown in the figure:

![](E:\UCLA\Blimp_project\Public_git_files\Tutorial-Controlling-multiple-control-boards-through-game-controllers\pics\Xbox-360_controller.svg.png) 

The corresponding mapping between game controller and function of the airship is in the following table:

| Game controller                          | Airship functions                        |
| ---------------------------------------- | ---------------------------------------- |
| Left stick ($\uparrow,\downarrow,\leftarrow,\rightarrow$) | forward, backward,turn left, turn right  |
| Right stick ($\uparrow,\downarrow,\leftarrow,\rightarrow$) | Go up, go down, head up, tail up         |
| left bumper (LB)                         | 50% speed                                |
| Right bumper (RB)                        | 100% full speed                          |
| Y                                        | To set searching camera back to forward position |
| X,Y                                      | To turn the searching camera to the left or right |
|                                          |                                          |

### Usage

The format of the command:

```
python game_controller.py --sys [OS] --sim 
```

- ​

**Example:**

Depends on different Computer OS your are using, you can type the following different commands

- For Windows:

  ```
  python game_controller.py --sys win
  ```

- For Ubuntu:

  ```
  python game_controller.py --sys lix
  ```

- For Mac

  ```
  python game_controller.py --sys mac
  ```

## Keyboard

### Installation

Navigate to the target directory:

```
cd
```

running as simulator option:



### Control interface 

[Some pictures here]

### Usage



