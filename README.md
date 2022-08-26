# Controlling-motors/PID control
## Contents
1) Controlling LED brightness using PID & photosensor
2) Controlling a hobby motor car using PID
3) Controlling a DC motor using a joystick
4) Controlling a stepper motor using a potentiometer

## 1) Controlling LED brightness using PID & photosensor
The setpoint is set to the desired brightness and the LED will adjust its brightness accordingly.
Use this [tutorial](http://www.yilectronics.com/Tutorials/Arduino_Basics/Tutorial_5_PID_Photocell/PIDPhotocell.html)

## 2) Controlling a hobby motor car using PID
The setpoint is set to the desired distance from the ultrasonic sensor and the car will move to this position.

## 3) Controlling a DC motor using a joystick
Moving the joystick up will make it turn in 1 direction and moving it down will make it turn in the other direction. The motor will turn at a higher speed as the joystick moves further towards the two extremes and is still when the joystick is in the neutral position. 

## 4) Controlling a stepper motor using a potentiometer
The code for this is in the examples for the stepper. 
For MotorKnob (controlling stepper position), make sure to adjust the code to that below. The following code will map the values from the potentiometer to the the number of steps the stepper is required to move.
```
int val = analogRead(0);
int step = map(val,0,1023,0,STEPS); //new code

stepper.step(step-previous); //changed to step

previous = step; //changed to step
```
