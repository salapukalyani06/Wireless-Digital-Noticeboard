# 📲 Wireless Digital Notice Board

Welcome to the Wireless Digital Notice Board System! 🖥️📲  
This project uses the **LPC2148 microcontroller** to display scrolling messages on a **4-panel LED matrix**. Messages are sent from a smartphone via **Bluetooth** 📱🔗 and saved in **EEPROM** 💾 to ensure persistence after power loss. It’s a **simple, secure 🔐, and effective** solution for schools 🎓, offices 🏢, or public places 🚌 — a smart way to share messages wirelessly! 🚀

---

## 📋 Project Overview

This system combines multiple hardware modules to build a smart and interactive wireless display solution. Features include:

- 🖥️ **Scrolling Message Display** on a 4-panel 8×8 dot matrix LED  
- 📱 **Bluetooth Connectivity** via HC-05 module for wireless input  
- 💾 **Persistent Storage** using AT24C256 EEPROM  
- 🔐 **Secure Updates** with passkey-protected messages (`@153Your Message$`)  
- 🔁 **Auto-Scrolling** stored messages until updated  
- 🧠 **Powered by LPC2148** microcontroller for fast and reliable control  

Ideal for campuses, offices, and public spaces needing dynamic, wireless communication.

---

## 🔧 Hardware Components

- LPC2148 (ARM7 Microcontroller)  
- 4 × 8×8 Dot Matrix LED Displays  
- HC-05 Bluetooth Module  
- AT24C256 EEPROM (I2C)  
- 74HC573 (Octal Latch)  
- 74HC164 (Shift Register)  

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

- Send messages via Bluetooth using passkey format (e.g., `@153Message$`)  
- Scroll long messages across 4 LED matrices  
- Store and retrieve messages from EEPROM  
- Continuous display until new message arrives  
- Default message display if EEPROM is empty  

---

## 🛠 Tools Used

- **Keil uVision** for embedded C development  
- **Flash Magic** for programming LPC2148  
- Embedded C programming language  

---

## 🚀 Usage Instructions

1. Flash the firmware onto LPC2148 using Flash Magic.  
2. Power on the board and pair your smartphone with the HC-05 module.  
3. Open a Bluetooth terminal app and send a message in the format:
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

