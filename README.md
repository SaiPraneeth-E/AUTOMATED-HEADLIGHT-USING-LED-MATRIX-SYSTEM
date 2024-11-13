Light and Obstacle Avoidance System for Arduino

This Arduino project is designed to navigate based on light detection and obstacle avoidance, making it perfect for robotic and automated systems. Using ultrasonic sensors, LDRs (Light Dependent Resistors), and servos, the system responds dynamically to environmental changes like obstacles and light levels.

Features

Obstacle Detection: Ultrasonic sensors monitor the left and right sides for obstacles. When an obstacle is detected within 10 cm, the corresponding servo rotates to avoid it.

Light Sensing: LDR sensors check ambient light levels. If the light surpasses a specified threshold, the servos and LEDs adjust based on proximity and light conditions.

Servo Control: Two servos create smooth rotations based on light and proximity detections, providing responsive motion control.

LED Headlights: Two LEDs simulate headlights, automatically turning on in response to specific light levels, simulating robotic adaptation to low-light conditions.

Hardware Components

Arduino Uno (or compatible board)

Ultrasonic Sensors (2x) - HC-SR04 or similar, for detecting obstacles on both sides

LDRs (2x) - Light Dependent Resistors to sense ambient light levels

Servos (2x) - For controlling movement in response to environmental cues

LEDs (2x) - Serve as headlights

Setup Instructions

Connect the ultrasonic sensors, servos, and LEDs to the Arduino according to the pin assignments specified in the code.

Set lightThreshold in the code to define the light intensity level at which the system responds.

Upload the code to your Arduino board.

How It Works

Detection Phase: The system reads data from ultrasonic sensors and LDRs.

Processing Phase:

If an obstacle is detected within 10 cm, the appropriate servo rotates to move the system away.
If light intensity is above the threshold, the headlights (LEDs) turn on.
Output Phase: The servos and LEDs adjust in real-time based on environmental changes.
This project is ideal for learning about Arduino sensors, servos, and environmental response mechanisms.
