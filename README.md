# Real-Time Motion Detection & Telegram Alert System Using ESP32-CAM

##  Project Overview
This project is a **real-time IoT-based smart security system** built using the **ESP32-CAM** module and a **PIR motion sensor**.  
The system detects motion, captures an image instantly, and sends it to the user via **Telegram**.  
Additionally, the ESP32-CAM hosts a **live video streaming server** accessible through a web browser.

> ⚠️ **Note:**  
> This project is developed by **modifying the official ESP32 CameraWebServer example** provided by Espressif and extending it with **PIR-based motion detection** and **Telegram photo alert functionality**.

---

## ✨ Key Features
- 🚶 Real-time motion detection using PIR sensor  
- 📸 Automatic image capture on motion  
- 📲 Instant photo alerts via Telegram  
- 🌐 Live video streaming over Wi-Fi  
- 🔌 Powered using a **stable 5V external adapter**  
- 💡 Low-cost & beginner-friendly IoT security project  

---

## 🧰 Hardware Components
- ESP32-CAM (OV2640)
- PIR Motion Sensor (HC-SR501)
- ESP32-CAM USB Programmer / FTDI
- 5V External Power Adapter (minimum 2A recommended)
- Jumper Wires
- Breadboard (optional)

---

## ⚙️ How the System Works
1. The PIR sensor continuously monitors for motion.
2. When motion is detected, a HIGH signal is sent to the ESP32-CAM.
3. ESP32-CAM captures an image using the camera module.
4. The image is sent instantly to the user via **Telegram Bot API**.
5. At the same time, ESP32-CAM runs a web server for **live video streaming**.

---

## 🛠️ Software & Tools Used
- Arduino IDE
- ESP32 Arduino Core
- Telegram App
- Wi-Fi Network

---

## 📥 ESP32 Board Setup
1. Open **Arduino IDE → File → Preferences**
2. Add the following URL to **Additional Board Manager URLs**:
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
3. Go to **Tools → Board Manager**
4. Search for **ESP32** and install it
5. Select:
   - Board: **ESP32 Wrover Module**
   - Partition Scheme: **Huge App**
   - Upload Speed: **115200**

---

## 🤖 Telegram Bot Setup
1. Open Telegram and search for **@BotFather**
2. Create a new bot using `/newbot`
3. Copy the **Bot Token**
4. Get your **Chat ID** using a Chat ID bot
5. Replace the following placeholders in the code:
   ```cpp
   const char* ssid = "YOUR_WIFI_NAME";
   const char* password = "YOUR_WIFI_PASSWORD";
   const char* botToken = "YOUR_BOT_TOKEN";
   const char* chatID = "YOUR_CHAT_ID";
   ```

⚠️ **Security Notice:**  
Never upload your real Wi-Fi credentials or bot token to a public repository.

---

## ▶️ How to Run the Project
1. Open the project folder in Arduino IDE
2. Upload the code to ESP32-CAM using a USB programmer
3. Open Serial Monitor (baud rate: 115200)
4. Press the **RESET** button on ESP32-CAM
5. Copy the IP address shown in Serial Monitor
6. Open the IP in a web browser to view live stream
7. Move in front of the PIR sensor to receive Telegram alerts

---

## 🎥 Demo Video
Watch the project in action on YouTube:  
👉 **Demo Video Link:** https://youtu.be/YOUR_DEMO_VIDEO_LINK

---

## 📁 Repository Structure
```
esp32-cam-telegram-motion-alert/
│
├── code/
│   ├── esp32_cam_telegram/
│   │   ├── esp32_cam_telegram.ino
│   │   ├── app_httpd.cpp
│   │   ├── camera_index.h
│   │   └── camera_pins.h
│   │
│   └── PIR_TESTING_CODE/
│       └── PIR_TESTING_CODE.ino
│
├── README.md
└── LICENSE
```

### 📄 PIR_TESTING_CODE.ino
This file is used for **independent testing and calibration of the PIR motion sensor** before integrating it with the ESP32-CAM system.

---

## 📜 License
This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project.

---

## 👨‍💻 Author
**Shahriar Alom Masud**  
B.Sc. Engg. in IoT & Robotics Engineering  
University of Frontier Technology, Bangladesh  
📧 Email: shahriar0002@std.uftb.ac.bd  
🔗 LinkedIn: https://www.linkedin.com/in/shahriar-alom-masud  

---
