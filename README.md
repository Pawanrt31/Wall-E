# Trash Collector System

The project consists of constructing a trash collector robot using LEGOs and TETRIX.
## Algorithm:
Step1:START
Step2:[clamp function]
Initialize the names of the motors A and C
Motor A as the master and motor C as its slave
nSyncedMotors=synchAC
nSynchedturnsratio=100
Step3:[Set encoders pulses value to turn clamp and declamp using encoder function]
        
[for clamping]

nMotorEncoder[B]=0
nMotorEncoderTarget[B]=100
motor[B]=-25

[set time for how long the process should be carried out]
wait1Msec(2000)

[for lifting the motor]	

nMotorEncoder[A]=0

nMotorEncoderTarget[A]=155

motor[A]=25

[ whole process of clamping to be carried out changing the values of respective encoders accordingly]

Step4:close clamp function

Step 5: [main function]

Initialise int ;

Step6:for(i=0;I greater than 10; i=i+1)
{
	
 Step7:[while the sensor value detected is greater than 20]
		while(SensorValue(sonar)>20)
		{
		[Power the dc motors]
	                 motor[rightMotor]=5;
		motor[leftMotor]=5;
		}
		
		motor[rightMotor]=0;
		motor[leftMotor]=0;
Step8:		clamp function is to be called
Step9: STOP

## Description:
1.The robot consists of 3 motors with servo motors attached to the motors. The motors are labelled as A,B,C.
2.Motor B is attached with the clamping mechanism, the motor rotates at a specific angle such that the mechanism that is attached to the motor appears like a robot hand clamping or holding
an object.
3.The motors A and C serve the locomotive functionality to the robot which facilitates in the robot's movement.
4. The two motors have to be in synch whenever they are moving hence synchroniztion is mentioned between A and C with A acting as master and C as slave.
5. The motor rotates for an angle of 180 degrees detecting any object in its vicinity with the help of ultrasonic sensor.
6. The robot moves for some distance forward, stops and scans the entire semicircle area in front of it to detect any object.
7. Upon detection of an object the clamping mechanism function is called which rotates motor B so that the object in front of the robot is held or clamped.
8. The detected object is collected in a tray or storage provided at the back of the robot.
