# LineFollowerBot


## Tools: 
1. Arduino UNO
2. L293D Motor Driver IC
3. Geared Motors x2
4. Robot Chassis
5. IR Sensor Module x2


## Brief:
In this project, I have designed an Arduino based Line Follower Robot.The design of this robot is such that it detects the black line on the surface and moves along that line.
I need sensors to detect the line. There are various sensors that detect the line, hurdles and follow the path. The sensor signals are fed into Arduino UNO and it sends signals to motor drivers accordingly.
I have used the Zigbee module for wireless communication and coded everything in Arduino.


## Working:
* For line detection logic, I used two IR Sensors, which consists of IR LED and Photodiode. They are placed in a reflective way i.e. side – by – side so that whenever they come in to proximity of a reflective surface, the light emitted by IR LED will be detected by Photo diode.In case of black surface, which has a low reflectance, the light gets completely absorbed by the black surface and doesn’t reach the photodiode.
* Using the same principle, we will setup the IR Sensors on the Line Follower Robot such that the two IR Sensors are on either side of the black line on the floor.
* When the robot moves forward, both the sensors wait for the line to be detected. For example, if the IR Sensor 1 in the above image detects the black line, it means that there is a right curve (or turn) ahead.
* Arduino UNO detects this change and sends signals to motor drivers accordingly. In order to turn right, the motor on the right side of the robot is slowed down using PWM, while the motor on the left side is run at normal speed.
