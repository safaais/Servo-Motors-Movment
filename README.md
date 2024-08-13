# Servo-Motors-Movment
•	This project uses an Arduino UNO board to control 6 servo motors, enabling the creation of a walking motion for a robot. The Servo library facilitates the precise control of the servo motors, allowing for the coordinated movement required for locomotion.


## •	Power: The red wire from the Arduino Uno board's 5V pin is connected to the positive rail of the breadboard, and the black wire from the GND pin is connected to the negative rail.
## •	Servos: The servos are connected to the breadboard as follows:
#### •	Servo 1: Red wire to 5V, black wire to GND, and orange wire to digital pin 9.
#### •	Servo 2: Red wire to 5V, black wire to GND, and orange wire to digital pin 10.
#### •	Servo 3: Red wire to 5V, black wire to GND, and orange wire to digital pin 11.
#### •	Servo 4: Red wire to 5V, black wire to GND, and orange wire to digital pin 12.



## The Code:

```
#include <Servo.h>

Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;

void setup() {
  servo1.attach(3);  // Connect servo 1 to pin 3
  servo2.attach(5);  // Connect servo 2 to pin 5
  servo3.attach(6);  // Connect servo 3 to pin 6
  servo4.attach(9);  // Connect servo 4 to pin 9
  servo5.attach(10); // Connect servo 5 to pin 10
  servo6.attach(11); // Connect servo 6 to pin 11
}

void loop() {
  // Move the servos to create a walking motion for the robot

  // Move servo 1 and 4 to 90 degrees
  servo1.write(90);
  servo4.write(90);
  delay(500);  // Wait for half a second

  // Move servo 2 and 5 to 45 degrees
  servo2.write(45);
  servo5.write(45);
  delay(500);  // Wait for half a second

  // Move servo 3 and 6 to 135 degrees
  servo3.write(135);
  servo6.write(135);
  delay(500);  // Wait for half a second

  // Return servos to original positions
  servo1.write(0);
  servo2.write(0);
  servo3.write(0);
  servo4.write(0);
  servo5.write(0);
  servo6.write(0);

  delay(1000);  // Wait for 1 second
}
```

## The Circuit:

