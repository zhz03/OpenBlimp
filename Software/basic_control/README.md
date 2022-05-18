# 0_Main Function of Blimp

## 1. CALIBRATION: Coupling the DC Motors, Motor Shield, and Code
### The codes, the propellers of the blimp, and the motor number in the featherboard are all coupled together -- dependent to each other. It is highly recommended that the user of this project determines the direction of each motor and list them.

<br>

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

