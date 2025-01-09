
# 🛠️ **Servo-Controlled Ultrasonic Distance Measurement**

This project demonstrates how to control a **servo motor** and measure distance using an **ultrasonic sensor**. The servo motor sweeps from **15° to 165°** and back, while the ultrasonic sensor calculates and reports the distance at each angle, displaying it in the **Serial Monitor**.

---

## 📋 **Components Required:**

- **Servo Motor** (connected to pin 12)
- **Ultrasonic Sensor (HC-SR04)**:
  - Trigger Pin (connected to pin 10)
  - Echo Pin (connected to pin 11)
- **Arduino Board** (or compatible microcontroller)

---

## 🔌 **Wiring Instructions:**

### Servo Motor:
- **Signal Pin**: Pin 12 (Arduino)
- **VCC Pin**: 5V (Arduino)
- **GND Pin**: GND (Arduino)

### Ultrasonic Sensor (HC-SR04):
- **Trigger Pin**: Pin 10
- **Echo Pin**: Pin 11
- **VCC Pin**: 5V (Arduino)
- **GND Pin**: GND (Arduino)

---

## ⚙️ **Libraries Used:**

- `Servo.h` — Controls the servo motor's movements.
- `Wire.h` — Enables I2C communication (if necessary for additional components).

---

## 📝 **Setup Instructions:**

### 1. Clone the Repository:
```bash
git clone https://github.com/your-username/servo-ultrasonic-distance.git
```

### 2. Upload the Code:
- Open the `servo_ultrasonic.ino` file in the **Arduino IDE**.
- Select the correct **board** and **port**.
- **Upload** the code to your Arduino board.

### 3. Connect the Hardware:
- Connect the **servo motor** to pin 12.
- Connect the **ultrasonic sensor** to pins 10 (Trig) and 11 (Echo).
- Provide power to the Arduino and components.

### 4. Monitor the Output:
- Open the **Serial Monitor** in the Arduino IDE.
- The servo will sweep from **15° to 165°** and back.
- The **angle** and **distance** will be displayed in the Serial Monitor in this format:
  ```
  angle,distance.
  ```

---

## 📊 **Code Explanation:**

- The **servo motor** rotates from **15° to 165°** and back, in **1-degree increments**.
- The **ultrasonic sensor** measures the distance at each angle, sending the result to the **Serial Monitor**.
- The distance is calculated using the formula:
  ```cpp
  distance = duration * 0.034 / 2;
  ```
  - `duration` is the time taken for the pulse to return.

---

## 📈 **Example Output:**

You will see data in the Serial Monitor, for example:
```
15,25.5.
16,24.9.
17,24.3.
...
165,18.1.
```
Where:
- **First value**: Angle of the servo motor (e.g., 15°)
- **Second value**: Distance measured by the ultrasonic sensor in centimeters (e.g., 25.5 cm)

---

## 🤝 **Contributing:**

If you'd like to contribute to this project, feel free to **fork** the repository and submit a **pull request** with your changes. All contributions are welcome!

---

## 📜 **License:**

This project is licensed under the [MIT License](LICENSE).

---
