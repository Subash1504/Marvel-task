# Equipments required 
- ESP32
- jumping wires
- OLED
- buzzer

To check if the OLED screen is working with your ESP32, you can run a simple test sketch that initializes the display and writes a message to it. Here's a step-by-step guide:

### Step 1: Install Libraries

1. **Adafruit SSD1306 Library**: This library is used to control the OLED display.
2. **Adafruit GFX Library**: This library provides graphics functions for the display.

You can install these libraries through the Arduino IDE:

- Go to **Sketch > Include Library > Manage Libraries**.
- In the Library Manager, search for "Adafruit SSD1306" and install it.
- Search for "Adafruit GFX" and install it.

### Step 2: Wire the OLED Display to the ESP32

- **SDA**: Connect to GPIO 21.
- **SCL**: Connect to GPIO 22.
- **VCC**: Connect to 3.3V.
- **GND**: Connect to GND.

### Step 3: Test Sketch

https://github.com/user-attachments/assets/b8a7ea00-eef9-462d-93a8-b097dc082851

![IMG-20240802-WA0003](https://github.com/user-attachments/assets/f8ef2ba9-6a77-4539-8b93-a44cffde71c9)
