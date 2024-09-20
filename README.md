![Resume_Subash_Chandra_Poornaraga_Colored](https://github.com/user-attachments/assets/8aecfaf5-9ff6-43c4-a160-d6ce2f1a06e0)




# Equipments required 
- ESP32
- Bread board
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
- Upload the following test sketch to your ESP32 to check if the OLED screen is working

### Step 4: Upload the Sketch

1. Connect your ESP32 to your computer via USB.
2. Open the Arduino IDE and select the correct board and port.
   - Go to **Tools > Board** and select **ESP32 Dev Module**.
   - Go to **Tools > Port** and select the correct COM port.
3. Click the **Upload** button to upload the sketch to your ESP32.

### Step 5: Verify the Display

After uploading the sketch, your OLED display should show the message "Hello, world!". If you see this message, the OLED screen is working correctly.

### Troubleshooting

If the display does not show the message, check the following:

1. **Wiring**: Ensure that the SDA, SCL, VCC, and GND connections are correct.
2. **I2C Address**: The default I2C address for many OLED displays is `0x3C`. If your display uses a different address, change the address in the `display.begin()` function:
   ```cpp
   if (!display.begin(SSD1306_I2C_ADDRESS, OLED_RESET)) {
   ```
   to
   ```cpp
   if (!display.begin(0x3D, OLED_RESET)) { // Replace 0x3D with your display's I2C address
   ```
3. **Power Supply**: Ensure the display is receiving enough power. The VCC pin should be connected to 3.3V.

By following these steps, you should be able to verify that your OLED screen is working properly with your ESP32.


https://github.com/user-attachments/assets/b8a7ea00-eef9-462d-93a8-b097dc082851

![IMG-20240802-WA0003](https://github.com/user-attachments/assets/f8ef2ba9-6a77-4539-8b93-a44cffde71c9)
