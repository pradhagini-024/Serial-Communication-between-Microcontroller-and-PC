# Send and receive data between a microcontroller (Arduino/ESP32) and a PC

Exp 4 Send and receive data between a microcontroller (Arduino/ESP32) and a PC.


**Aim**
To send and receive data between an Arduino UNO microcontroller and a PC using serial communication through the Arduino IDE Serial Monitor.

**Apparatus Required**
•	Arduino UNO
•	USB cable
•	Computer/PC
•	Arduino IDE

**Circuit / Connection**

Connect the Arduino UNO to the PC using a USB cable. No external circuit is required.
 
<img width="602" height="195" alt="image" src="https://github.com/user-attachments/assets/a94ea03e-7454-4215-bcba-6dd280cb0988" />


**Procedure**
1.	Connect the Arduino UNO to the PC using the USB cable.
2.	Open Arduino IDE and select Arduino UNO and the correct COM port.
3.	Enter and upload the program given below.
4.	Open the Serial Monitor and set the baud rate to 9600.
5.	Observe the message sent from Arduino to the PC.
6.	Enter a message in the Serial Monitor and observe the received message.

**Arduino IDE Code**
```
void setup() {
  Serial.begin(9600);
  Serial.println("Hello from Arduino");
}

void loop() {
  // Send data from Arduino to PC
    // Receive data from PC
  if (Serial.available() > 0) {
    char receivedData = Serial.read();

    Serial.print("Received: ");
    Serial.println(receivedData);
  }

  delay(1000);
}
```

**Output:**

<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/21841516-6942-4e93-b271-1d7b49d29e3f" />

**Result**
Data was successfully sent and received between the Arduino UNO and the PC using serial communication through the Arduino IDE Serial Monitor


