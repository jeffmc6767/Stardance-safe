This readme was made using AI: - BUT DOUBLE CHECKED BY REAL HUMAN AND ALL INFORMATION IS VALID

ESP32 Smart Desk Safe

A simple smart safe built using an ESP32, an RFID reader, an OLED display, a servo motor, and a buzzer. Scan an authorized RFID card to lock or unlock the safe. The OLED displays the current status, and the buzzer provides audio feedback.

⸻

Features

* RFID card authentication
* OLED status display
* Servo locking mechanism
* Buzzer feedback
* External servo power support

⸻

Components

* ESP32 DevKit V1 (ELEGOO)
* RC522 RFID Reader
* 0.96” OLED Display (SSD1306 I2C)
* SG90 Servo
* Active Buzzer
* External 5V Power Supply (recommended)
* Breadboard
* Jumper Wires

⸻

Wiring

OLED

OLED	ESP32
VCC	3.3V
GND	GND
SDA	GPIO 21
SCL	GPIO 22

⸻

RFID (RC522)

RC522	ESP32
SDA	GPIO 5
SCK	GPIO 18
MOSI	GPIO 23
MISO	GPIO 19
IRQ	Not Connected
GND	GND
RST	GPIO 27
3.3V	3.3V

Do NOT connect the RC522 to 5V.

⸻

Servo

Servo	Connection
Signal (Orange/Yellow)	GPIO 13
Power (Red)	External 5V
Ground (Brown/Black)	External GND

⸻

Buzzer

Buzzer	ESP32
+	GPIO 26
-	GND

⸻

Power

Power the ESP32 using the USB-C cable.

Power the servo using an external 5V power supply.

Connect the external power supply GND to an ESP32 GND pin.

Do not power the servo from the ESP32.

⸻

GPIO Summary

GPIO	Device
5	RFID SDA
13	Servo Signal
18	RFID SCK
19	RFID MISO
21	OLED SDA
22	OLED SCL
23	RFID MOSI
26	Buzzer
27	RFID RST

⸻

Arduino Libraries

Install these libraries using the Arduino Library Manager:

* Adafruit GFX Library
* Adafruit SSD1306
* MFRC522
* ESP32Servo

⸻

Arduino Settings

Board:

ESP32 Dev Module

Upload Speed:

115200

⸻

RFID Card

Replace the UID in the code with your own RFID card if needed.

Current UID:

04 E7 67 07 CC 2A 81

⸻

Uploading

1. Connect the ESP32 with USB.
2. Open the Arduino sketch.
3. Select ESP32 Dev Module.
4. Select the correct COM/Serial Port.
5. Click Upload.

If uploading fails, disconnect the servo and external power, upload again, then reconnect everything.

⸻

Using the Safe

1. Power the ESP32.
2. Power the servo with the external 5V supply.
3. The OLED will display Scan Card.
4. Scan the authorized RFID card.
5. The servo will lock or unlock.
6. The OLED will display the current status.
7. The buzzer will beep once for access granted and twice for access denied.

⸻

Troubleshooting

OLED stays black

* Check SDA is connected to GPIO 21.
* Check SCL is connected to GPIO 22.
* Make sure the OLED I2C address is 0x3C.

RFID does not read cards

* Make sure it is powered from 3.3V.
* Check all SPI wiring.
* Verify the card UID in the code matches your RFID card.

Servo jitters or resets the ESP32

* Power the servo from an external 5V supply.
* Connect the external power supply GND to ESP32 GND.
* Do not power the servo from the ESP32.

Upload fails

* Disconnect the servo while uploading.
* Use a good USB data cable.
* Try an upload speed of 115200.

⸻

Current Status

✅ RFID authentication

✅ OLED display

✅ Servo lock

✅ Buzzer feedback

🚧 Keypad support coming soon

🚧 Ultrasonic sensor

🚧 Custom 3D printed enclosure

🚧 Custom PCB
