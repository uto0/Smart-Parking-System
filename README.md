# 🚗 Smart Parking System with ESP32

This is a complete Smart Parking system built using ESP32 and C++. It allows users to reserve a parking spot via a local web interface. Once reserved, if the spot is available, the servo motor opens the gate automatically.

## 🔧 Features

- Wi-Fi Access Point hosted by ESP32
- Reservation via web browser
- Real-time parking status (Occupied / Available)
- Servo-controlled gate
- IR or Ultrasonic vehicle detection
- Visual indicator using LED

---

## 🧠 How It Works

1. ESP32 monitors the parking spot using a sensor.
2. A green LED indicates availability; red means occupied.
3. A user connects to the ESP32's WiFi and opens the web interface.
4. Upon pressing the "Reserve" button:
   - If the spot is free, the servo opens the gate for 5 seconds.
   - If the spot is taken, reservation is denied.

---

## 📡 Hardware Connections

| Component         | ESP32 GPIO |
|------------------|------------|
| IR / Ultrasonic   | GPIO 32    |
| LED              | GPIO 2     |
| Servo Motor      | GPIO 4     |

---

## 📁 File Structure

- `firmware/SmartParking.ino`: Main Arduino code
- `data/index.html`: Web page served from ESP32 SPIFFS
- `README.md`: Project overview and setup guide

---

## ⚙️ Setup

1. Install Arduino IDE with ESP32 board support.
2. Install required libraries:
   - ESP32Servo
   - ESPAsyncWebServer (if needed for advanced features)
3. Upload `SmartParking.ino` to your ESP32.
4. Upload `index.html` to SPIFFS using ESP32FS tool.

---

## 🌐 Web Interface

- After uploading, connect to the WiFi:
  - SSID: `SmartParking`
  - Password: `12345678`
- Visit `http://192.168.4.1` to access the reservation page.

---

## 📷 Preview

![Smart Parking System Schematic](https://example.com/schematic.png)

---

## 📌 Future Enhancements

- Integration with Firebase or MQTT
- Display available spots on LCD or mobile app
- User authentication and admin panel

---

## 👤 Author

insta >> @B9R7 
Language: C++  
Platform: ESP32

---

## 📝 License

This project is open-source under the MIT License.
