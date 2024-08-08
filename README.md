## RobotArm-Control-Software
Put EXE file and Dpack in the same folder

**This application is still undercontruction**

https://www.youtube.com/shorts/FX_H2kLgglc

https://www.youtube.com/watch?v=CckkPZei0uk

Inverse Kinematic Test

https://www.youtube.com/watch?v=r0UIWNHXIsQ

https://www.youtube.com/watch?v=weg_Roc70cU

Application Demo Video

https://youtu.be/nj29ULLXav4


Vision system demo

https://www.youtube.com/watch?v=CckkPZei0uk

## How to use this application

Note: 
+ Before using this application to control your robot arm, please input your robot's parameter in Robot Congifuration Tab.
+ Number of steps each joint has to move is calculated in this application, MCU will receive the message with the specific value in STEP number.
+ You can adjust the step number by changing Reduction Ratio for each joints.
+ Upper Limit and Lower Limit is based on your actual working range of your arm.
+ Calibrate to home: to set up the moving distance from the calibrate switch to Home.

!!! Serial Communication will be explained clearly for each function. 

!!! The overal routine of Serial Communication is to send the message to MCU and wait for "Ok" message sent from MCU for each action.

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/e1819ec2-6fb8-4c52-b119-23baf3859d3e)

## Serial configuration

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/61e50795-bd00-4d18-9cdd-f7bab7aeec3d)

PORT: To choose avaiable port to connect to MCU

BAUDRATE: To set Baudrate.

## Basic Function

These Function to set speed, accelerate. and to calibrate joints or set robot arm to home position.

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/6f51a7a2-9e0e-4428-9d8e-0a7ee858d735)

Use checkbox to choose joints to be calibrated or set home.

Use check All to choose all joints.

The message type sent to arduino :
  + for calibrate: CA(calibrate_Status)B(calibrate_Status)C(calibrate_Status)D(calibrate_Status).....F(calibrate_Status)

For set to home position, Send the Moving message to Home position.

## Moving Parameter

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/c2bb3b6f-cae8-4f09-b352-d04a062630b5)


To Move the arm by specific Angle(forward kinetics)
 + Enter angle value and click move
 + To access gripper in the movement, use slider to choose value for Gripper.
   
!!!This application will convert the angle base on your input parameter to step and send it to MCU
After Moving, the application will display the Pose of the arm in Pose section( Orientation and Position)

**Message form: DA(numStep)B(numStep)C(numStep)D(numStep)E(numStep)F(numStep)G(GripperStatus)**

To Move the arm by Pose( inverse Kinetics)
 + Enter your expected Pose
 + The Application will calculate the inverse kinetic equation of the Arm to get the angle eachs joint has to move.
 + The angle value will be converted to step and sent to MCU
   
**Message form: DA(numStep)B(numStep)C(numStep)D(numStep)E(numStep)F(numStep)G(GripperStatus)**

**Interpolation Movement**
 + Click the check box to choose interpolation movement type
 + Enter Res(mm) (Resolution for linterpolation)
 + 
## Robot arm V2

  ![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/4dad62fd-54d2-46e7-a9e9-754eeff4baba)

  ![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/3fb6742c-95cf-47ec-80ce-1c7ea0ba8af8)

  ![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/4d998acf-11e5-4787-b590-45d9b8333a38)

  ![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/5baaf6f2-ea71-40ad-8550-ff760b403602)

## Robot arm V2 3D- Model

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/a30de161-779a-41eb-b42d-172bae49d36e)

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/55850852-e81f-4453-bcb5-bde61f33f4ac)

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/ec44bac4-4d94-442a-bcc3-fd990bc4f4ee)

![image](https://github.com/phamhduc/RobotArm-Control-Software/assets/101264143/6eb2bfcb-ffe5-4eb2-b3ae-b020d690d404)


This robot arm is designed to be 3D-printable using a 3D printer with a minimum working dimemsion of 220x220x300 mm.


The 3D model will be published soon
