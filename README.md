# IoT-Rubber-Ducky-Using-Arduino-Micro-Controller
Showcasing How Rubber Ducky Is really annoying


"A project leveraging the Arduino Microcontroller for simulating Rubber Ducky scripts and automating payload delivery."

---

## Overview

This project demonstrates how to use an **Arduino Microcontroller** to simulate the behavior of a Rubber Ducky, delivering automated scripts when connected to a PC. Rubber Ducky devices are often used for ethical hacking, penetration testing, and automating repetitive tasks. This guide provides a comprehensive walkthrough for beginners while emphasizing ethical use.

---

## Hardware Requirements

To build this project, you will need:

- **Arduino Microcontroller Board**: Compatible boards include Arduino Pro Micro, Leonardo, or other ATmega32U4-based boards that support HID (Human Interface Device).
  
  ![Arduino Microcontroller](src/Source/arduino_micro.jpg)

- **USB Cable**: For connecting the Arduino board to a PC.

- **PC or Laptop**: Required for coding and flashing scripts onto the Arduino.

- **Microcontroller Case (Optional)**: To protect the device and make it more portable.

---

## Software Requirements

- **Arduino IDE**: Available for free at [Arduino's official website](https://www.arduino.cc/en/software).

- **DuckScript Encoder**: Tools such as `DuckEncoder` or `DuckyScript` compiler for converting scripts into Arduino-compatible payloads.

- **Required Libraries**: Install the **HID-Project** library in Arduino IDE for handling keyboard and mouse emulation.

---

## Project Features

### Key Functionalities

1. **Automated Script Execution**: Runs predefined scripts upon connection to a PC.
2. **Customizable Payloads**: Easily modify payloads for various use cases.
3. **Portability**: Compact and portable design for easy deployment.

### Example Use Cases

- Simulating keystrokes for automated tasks.
- Demonstrating phishing attacks for educational purposes.
- Testing system vulnerabilities as part of penetration testing.

---

## Getting Started

### Step 1: Install Arduino IDE

1. Download the Arduino IDE from [Arduino's official website](https://www.arduino.cc/en/software).
2. Install and open the IDE.

### Step 2: Configure the Arduino IDE

1. Go to **File** -> **Preferences**.
2. Add the following URL to the **Additional Boards Manager URLs** field:  
   `https://adafruit.github.io/arduino-board-index/package_adafruit_index.json`
3. Navigate to **Tools** -> **Board** -> **Boards Manager** and install the necessary packages for your Arduino board.

### Step 3: Install HID-Project Library

1. Open the Arduino IDE.
2. Go to **Sketch** -> **Include Library** -> **Manage Libraries**.
3. Search for **HID-Project** and click **Install**.

### Step 4: Write Your Payload

1. Write your payload in **DuckyScript**, e.g.:
   ```
   DELAY 500
   STRING Hello, this is a test script!
   ENTER
   ```
2. Use a DuckyScript encoder to convert it into Arduino-compatible code.

### Step 5: Upload the Code

1. Connect your Arduino board to the PC using a USB cable.
2. Select the appropriate board and port under the **Tools** menu.
3. Paste the generated code into the Arduino IDE and click **Upload**.

---

## Example Code

```c++
#include <HID-Project.h>

void setup() {
  // Initialize HID functionality
  Keyboard.begin();
  delay(500);

  // Payload execution
  Keyboard.print("Hello, this is a test script!");
  Keyboard.write(KEY_RETURN);
}

void loop() {
  // Loop is empty as the payload runs once
}
```

---

## Ethical Guidelines

This project is intended for **educational purposes only**. Misuse of these tools for malicious purposes may violate laws and ethical standards. Always ensure that you have proper authorization before testing systems or networks.

---

## Limitations

- **Device-Specific Compatibility**: Only works on systems that recognize HID devices.
- **Payload Complexity**: Advanced payloads may require additional coding skills.
- **Ethical Constraints**: Unauthorized use is illegal and unethical.

---

## Credits

- **HID-Project Library**: [HID-Project GitHub Repository](https://github.com/NicoHood/HID)
- **DuckScript Encoder**: Tools for converting payloads.

---

## Disclaimer

This guide is for educational purposes only. Unauthorized use of this project is strictly prohibited and may result in legal consequences.

