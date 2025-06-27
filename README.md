# Codetech_task_3
COMPANY: CODTECH IT SOLUTIONS

NAME:KANDHI.AKHIL

INTERN ID:CT04DF1663

DOMAIN: Embedded Systems

DURATION: 4 WEEKS

MENTOR: Neela Santhosh Kumar
DESCRIPTION : To read and display temperature data from a sensor on an LCD or serial monitor using an Arduino, you'll need to connect a temperature sensor (like LM35 or DHT11) to your Arduino board, write a sketch that reads the sensor data, converts it to a readable temperature value, and then outputs it to either the serial monitor or an LCD screen. Here's a step-by-step guide:

Hardware Setup: Connect the sensor: Connect the temperature sensor to the Arduino board. For example, with an LM35, connect the VCC pin to 5V, the GND pin to GND, and the output pin to an analog input pin (e.g., A0). Connect the LCD (optional): If using an LCD, connect its VCC and GND pins to the Arduino's 5V and GND, and the SDA and SCL pins to the Arduino's SDA and SCL pins (usually A4 and A5). If using a parallel LCD, you'll need to connect its data pins (D4-D7) and control pins (RS, EN) to digital pins on the Arduino. Breadboard and Jumper Wires: Use a breadboard and jumper wires to connect the components neatly.
Software Setup (Arduino IDE): Include Libraries: If using an LCD, include the necessary libraries, like LiquidCrystal.h or Wire.h (for I2C LCDs). If using a DHT sensor, include DHT.h. Define Pins and Variables: Define the pins used for the sensor and LCD, and any variables needed for temperature calculations. Setup Function: Initialize serial communication (if using serial monitor): Serial.begin(9600). Initialize the LCD (if using LCD): lcd.begin(16, 2) (for a 16x2 LCD). Loop Function: Read Sensor Data: Use analogRead(sensorPin) for analog sensors like LM35, or sensor-specific functions (e.g., DHT.read11(DHT11_PIN)) for digital sensors like DHT11. Convert to Temperature: Use the appropriate formula to convert the sensor reading to Celsius or Fahrenheit. For LM35, you can use voltage = reading * (5.0 / 1024.0); temperatureC = voltage * 100. Serial Monitor: Use Serial.print() and Serial.println() to display the temperature value. LCD: Use lcd.setCursor() and lcd.print() to display the temperature on the LCD. You can also use functions like lcd.clear() to refresh the display. Delay: Add a small delay (e.g., delay(1000)) to control the update frequency.

CIRCUIT DIAGRAM:

![image](https://github.com/user-attachments/assets/42cc4344-5946-46a2-927f-61a40f890f6a)

CODE :

const int sensorPin = A0;

void setup() { Serial.begin(9600); }

void loop() { int reading = analogRead(sensorPin); float voltage = reading * 5.0 / 1024.0; float temperatureC = voltage * 100;

Serial.print("Temperature: "); Serial.print(temperatureC); Serial.println(" °C");

delay(1000); }


OUTPUT:

![image](https://github.com/user-attachments/assets/68445c52-76a2-416f-b2b4-600a76e626c6)
![image](https://github.com/user-attachments/assets/6a1ca481-9faa-4adc-a95e-8b9e7ce5a6d2)

OUTPUT DEMONSTRATION :

https://www.youtube.com/watch?v=Mp_-KgOtIJo





