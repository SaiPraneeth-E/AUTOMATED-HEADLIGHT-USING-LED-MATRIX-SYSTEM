This project is designed to demonstrate a simple light and obstacle avoidance system using an Arduino. It utilizes sensors to detect both light levels and obstacles in the environment, adjusting the behavior of a robot or device in response. The key components include ultrasonic sensors, LDRs (Light Dependent Resistors), servos, and LEDs. The project can be useful for building autonomous robots or systems that need to navigate and react to changing conditions.

Key Features and Components
Obstacle Detection (Ultrasonic Sensors):

The ultrasonic sensors are used to measure the distance to nearby objects (obstacles). They work by emitting a sound pulse and measuring the time it takes for the echo to return.
There are two ultrasonic sensors in the system:
Left ultrasonic sensor: Measures the distance on the left side of the device.
Right ultrasonic sensor: Measures the distance on the right side.
If an obstacle is detected within 10 cm (you can adjust this threshold in the code), the system will react by adjusting the servos to avoid the obstacle, typically by moving in a different direction.
Light Detection (LDRs):

LDRs (Light Dependent Resistors) are used to detect the intensity of ambient light. As the light intensity increases, the resistance of the LDR decreases, providing an analog signal to the Arduino.
The system uses two LDRs:
Left LDR: Detects light levels on the left side of the system.
Right LDR: Detects light levels on the right side.
The system uses these light readings to decide whether to activate the headlights (LEDs) or adjust the servos to different positions based on whether there’s enough light.
Servo Control:

The project uses two servos to control the movement of the device. Servos are controlled by varying the angle at which they rotate.
Left Servo: Controls movement to the left based on proximity and light conditions.
Right Servo: Controls movement to the right and adjusts to avoid obstacles when detected.
The servos move smoothly by gradually adjusting the angle over a short delay, which helps avoid jerky or erratic movements.
LED Headlights:

Two LEDs are used to simulate headlights. These headlights turn on when the ambient light is below a certain threshold (detected by the LDRs), simulating the behavior of a vehicle or robot that adapts to low-light environments.
How It Works
Step 1: Light Detection: The system continuously reads the light levels from the LDRs. If the light intensity is greater than a predefined threshold, the system keeps the headlights (LEDs) off. If the light intensity drops below the threshold, the headlights turn on.

Step 2: Obstacle Detection: The system also constantly measures the distance to nearby obstacles using the ultrasonic sensors. If an obstacle is detected within a certain range (e.g., less than 10 cm), the system takes action:

It adjusts the servos to steer away from the obstacle (typically rotating the servos to move left or right).
Step 3: Servo Control: The servos adjust based on both light conditions and obstacle proximity:

If the left sensor detects light and there is an obstacle nearby, the system will move the left servo to avoid the obstacle.
If there is no obstacle detected, the servos will return to their default positions.
Step 4: Output (Headlights & Servo Movement):

When enough light is detected, the headlights (LEDs) are turned off. If it is dark, the headlights turn on.
The servos move based on the proximity of obstacles, and they adjust smoothly to avoid collisions.
Applications
Autonomous Robots: This system is ideal for autonomous robots that need to navigate a room or area while responding to obstacles and varying light conditions.
Smart Lighting Systems: The light detection mechanism could be applied to systems that automatically adjust lighting based on ambient light levels, such as in smart homes.
Obstacle Avoidance: This setup could be used in vehicles or mobile devices that need to detect obstacles and avoid collisions automatically.
