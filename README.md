# Wireless Digital Notice Board
📲 Welcome to the Wireless Digital Notice Board System! 🖥️🚀
This innovative system leverages the LPC2148 microcontroller to wirelessly display scrolling messages on a 4-panel LED matrix. Messages are sent in real-time from a smartphone via Bluetooth (HC-05) 📱🔗 and securely stored in EEPROM (AT24C256) 💾, ensuring they persist even after power loss. Designed for schools 🎓, offices 🏢, and public spaces 🚌, this solution offers a reliable, secure 🔐, and energy-efficient way to broadcast updates without manual intervention bringing smart communication to the next level!

---
## 📋 Project Overview

This project brings together multiple hardware modules to build a smart and interactive wireless display system. Here’s what it does:
🖥️ **Displays Messages**: Shows scrolling text on a 4-panel 8×8 dot matrix LED display.

📱 **Bluetooth Connectivity**: Accepts messages wirelessly from a smartphone using the HC-05 Bluetooth module.

💾 **EEPROM Storage**: Saves messages in AT24C256 EEPROM so they remain even after the device is powered off.

🔐 **Secure Message Update**: Only updates messages that come with a valid passkey (`@153Your Message$`).

🔁 **Auto-Scroll Display**: Continuously scrolls stored messages until a new one is received.

🧠 **Built on LPC2148**: Uses the ARM7-based LPC2148 microcontroller for fast and reliable control.

This system is easy to use, secure, and ideal for campuses, offices, and public spaces where digital communication is essential. 🚀

---
## 🔧 Hardware Components
- **LPC2148** (ARM7 Microcontroller)
- **4 × 8×8 Dot Matrix LED Displays**
- **HC-05 Bluetooth Module**
- **AT24C256 EEPROM** (I2C-based)
- **74HC573** (Octal Latch)
- **74HC164** (Shift Register)

---

## 📂 Project Structure
```
Major_Project/
├── delay.c / delay.h          # Custom delay functions
├── dml.c / dml.h              # Dot matrix LED control
├── i2c.c / i2c.h              # I2C protocol implementation
├── i2c_eeprom.c / .h          # EEPROM read/write functions
├── uart.c / uart.h            # UART communication
├── defines.h                  # Global definitions
├── projectmain.c              # Main source file
```

---

## 💡 Features
- Send text messages via Bluetooth using a passkey (e.g., `@153Message$`)
- Scroll long messages across all 4 LED matrices
- Store and retrieve messages using EEPROM (AT24C256)
- Continuously display stored messages until a new one is received
- Default message shown if EEPROM is empty

---

## 🛠 Tools Used
- **Keil uVision** (Embedded C development)
- **Flash Magic** (Programming LPC2148)
- **Embedded C Language**

---

## 🚀 How to Use
1. Flash the firmware using Flash Magic onto LPC2148.
2. Power on the board and connect your smartphone to **HC-05**.
3. Use a terminal app to send a message like:
   ```
   @153Hello World$
   ```
4. The system will:
   - Validate the passkey
   - Store the message in EEPROM
   - Scroll it on the LED display

---

## ✅ Status
- Bluetooth communication ✔️  
- EEPROM read/write ✔️  
- 4-panel dot matrix scrolling ✔️  
- UART + I2C integration ✔️  
- Passkey-based security ✔️  

---
## 🔧 Improvements & Future Enhancements

- **LCD Integration 📟**: While this project uses 8×8 dot matrix displays, it can be extended to work with an LCD (like 16x2 or graphical LCDs) for clearer, more flexible message display.   
- **Mobile App Interface 📱**: Create a simple Android app to send and manage messages easily over Bluetooth.  
- **Multi-Language Support 🌐**: Enhance character encoding to support local languages or symbols.  
- **Power Efficiency 💡**: Use LPC2148’s low-power modes to reduce energy consumption in idle states.  
- **Message Management 🗂️**: Implement EEPROM history to view or restore previously displayed messages.  
---
## 🤝 Contributing

Contributions are welcome! 🙌  
Feel free to fork this repository, improve features, fix bugs, or suggest enhancements.  
Submit a pull request and be a part of making this project even better! 😊

---

## 🙏 Acknowledgments

- The **LPC2148 developer community** for excellent documentation and tools.  
- The creators of **Keil** and **Flash Magic** for making embedded development easier.  
- Special thanks to **our mentors and team members** who guided and contributed to the development of this project.  
- And **you**, for exploring, using, or contributing to this project! 🎉

---

**Happy Coding!** 💻✨  
Let's keep sharing messages, wirelessly and smartly! 🖥️📲🚀

🎓 Developed by: *Veeranjaneyulu Vaddineni* 
🏫 Major Project  
🎯 Tech: LPC2148, Embedded C, 8*8 LED Matrix, HC-05(Bluetooth), AT24C256(EEPROM).

