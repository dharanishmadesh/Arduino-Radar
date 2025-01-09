
# Servo-Controlled Ultrasonic Distance Measurement

This project uses a servo motor and an ultrasonic sensor to measure distances at various angles. The servo motor sweeps from 15° to 165° and back, while the ultrasonic sensor measures the distance to an object in front of it at each angle. The measured distance is displayed in the Serial Monitor.

## Components Required:
- **Servo Motor** (connected to pin 12)
- **Ultrasonic Sensor (HC-SR04)**:
  - Trigger Pin (connected to pin 10)
  - Echo Pin (connected to pin 11)
- **Arduino Board** (or compatible microcontroller)

## Wiring:
- **Servo Motor**: 
  - Connect the signal wire to pin 12 on the Arduino.
  - Connect the power and ground pins to the appropriate 5V and GND pins.
  
- **Ultrasonic Sensor (HC-SR04)**: 
  - Trigger Pin: Pin 10
  - Echo Pin: Pin 11
  - VCC: 5V
  - GND: GND

## Libraries Used:
- `Servo.h`: Controls the servo motor.
- `Wire.h`: Enables I2C communication (if necessary for additional components).

## Setup Instructions:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/servo-ultrasonic-distance.git
   ```

2. **Upload the Code**:
   - Open the `servo_ultrasonic.ino` file in the Arduino IDE.
   - Select the correct board and port.
   - Upload the code to your Arduino board.

3. **Connect the Hardware**:
   - Connect the servo motor to pin 12.
   - Connect the ultrasonic sensor to pins 10 (Trig) and 11 (Echo).
   - Provide power to the board and components.

4. **Monitor the Output**:
   - Open the Serial Monitor in the Arduino IDE.
   - The servo will sweep from 15° to 165° and back.
   - The current angle and the corresponding distance measured by the ultrasonic sensor will be displayed in the format:
     ```
     angle,distance.
     ```

## Code Explanation:
- The servo motor sweeps from 15° to 165° and back in steps of 1 degree.
- At each angle, the ultrasonic sensor calculates the distance and sends the data to the Serial Monitor.
- The formula used to calculate the distance is:
  ```cpp
  distance = duration * 0.034 / 2;
  ```
  Where `duration` is the time taken for the pulse to return.

## Example Output:
In the Serial Monitor, you will see the following output:
```
15,25.5.
16,24.9.
17,24.3.
...
165,18.1.
```
Where the first value is the angle of the servo and the second value is the distance measured by the ultrasonic sensor in centimeters.

## Contributing:
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with your changes.

