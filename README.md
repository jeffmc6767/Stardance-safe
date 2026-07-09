This project is for the Stardance challenge by hackclub if you have any questions please let me know so I can help
🔐 ESP32 Smart Desk Safe

A simple smart safe built with an ESP32. Scan an authorized RFID card to lock or unlock the servo, view the status on the OLED display, and hear buzzer feedback.

⸻

Parts

* ESP32 DevKit V1
* RC522 RFID Reader
* 0.96” I2C OLED Display
* SG90 Servo
* Active Buzzer
* External 5V Power Supply
* Breadboard & Jumper Wires

⸻

Wiring

| **Device**       | **Device Pin**              | **Connect to ESP32**                                    |
| ---------------- | --------------------------- | ------------------------------------------------------- |
| **OLED Display** | VCC                         | **3.3V**                                                |
|                  | GND                         | **GND**                                                 |
|                  | SDA                         | **GPIO 21**                                             |
|                  | SCL                         | **GPIO 22**                                             |
| **RC522 RFID**   | SDA (SS)                    | **GPIO 5**                                              |
|                  | SCK                         | **GPIO 18**                                             |
|                  | MOSI                        | **GPIO 23**                                             |
|                  | MISO                        | **GPIO 19**                                             |
|                  | RST                         | **GPIO 27**                                             |
|                  | GND                         | **GND**                                                 |
|                  | 3.3V                        | **3.3V**                                                |
| **Servo**        | Signal (Orange/Yellow wire) | **GPIO 13**                                             |
|                  | Power (Red wire)            | **External 5V**                                         |
|                  | Ground (Brown/Black wire)   | **External GND** _(must also connect to the ESP32 GND)_ |
| **Buzzer**       | +                           | **GPIO 26**                                             |
|                  | -                           | **GND**                                                 |

Important: Connect the external power supply GND to an ESP32 GND.

⸻

Setup

1. Install Arduino IDE

Download and install the Arduino IDE.

⸻

2. Install the ESP32 Board

In Arduino IDE:

* Open Boards Manager
* Search for ESP32
* Install Espressif ESP32

⸻

3. Install Libraries

Open Library Manager and install:

* Adafruit GFX Library
* Adafruit SSD1306
* MFRC522
* ESP32Servo

⸻

4. Open the Code

Open the "PROJECT CODE" file included in this repository. and paste it into ARDUINO IDE

⸻

5. Select Your Board

Choose:

ESP32 Dev Module

⸻

6. Select Your Port

Choose the serial port for your ESP32.

⸻

7. Upload

Click Upload.

If the upload fails, disconnect the servo power and try again.

⸻

8. Power the Servo

After the upload finishes:

* Connect the external 5V power supply.
* Make sure the external GND is connected to ESP32 GND.

⸻

9. Scan Your RFID Card

Edit the code and replace the UID with your own RFID card if needed.

Current UID:

04 E7 67 07 CC 2A 81 - replace this with your NFC card UID

⸻

How It Works

1. Power on the ESP32.
2. The OLED will display Scan Card.
3. Scan the authorized RFID card.
4. The servo will lock or unlock.
5. The OLED displays the status.
6. The buzzer provides feedback.

⸻

Current Features

* RFID Authentication
* OLED Status Display
* Servo Lock
* Active Buzzer Feedback

More features such as a keypad, ultrasonic sensor, and custom enclosure will be added in future updates.
