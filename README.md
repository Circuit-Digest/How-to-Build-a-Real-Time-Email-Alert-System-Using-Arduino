# 📧 Real-Time Email Alert System Using Arduino

## 🚀 Arduino Based Email Alert System (Temperature Monitoring)

This project demonstrates how to build a Real-Time Email Alert System using Arduino Uno R4 and a DHT11 temperature sensor.

When the temperature exceeds a predefined threshold, the Arduino automatically sends an email notification using a secure HTTPS connection through the CircuitDigest Cloud Email Notification API.

This system is ideal for real-time monitoring and IoT-based alert applications.

---

## 🧠 Project Overview

The Arduino Uno R4 continuously monitors temperature and humidity using the DHT11 sensor.

When:
- Temperature remains within normal range → System keeps monitoring
- Temperature exceeds threshold → Email alert is triggered

The system:
- Connects to WiFi
- Sends secure HTTPS request
- Delivers real-time email notification
- Prevents repeated alerts using control logic

This creates a reliable Arduino email alert system.

---

## 🛠️ Components Required

| Component | Quantity |
|------------|----------|
| Arduino UNO R4 | 1 |
| DHT11 Sensor | 1 |
| Breadboard | 1 |
| Connecting Wires | As required |

---

## 🔌 Circuit Connections

| DHT11 Pin | Arduino UNO R4 |
|-----------|----------------|
| VCC | 5V |
| GND | GND |
| DATA | Digital Pin 2 |

Digital Pin 2 is configured to read temperature and humidity data from the DHT11 sensor.

---

## ⚙️ Working Principle

1. Arduino initializes WiFi and DHT11 sensor.
2. Temperature and humidity are read at fixed intervals.
3. Temperature is compared with a threshold value.
4. If temperature > threshold:
   - Email alert is triggered.
5. A control flag prevents repeated emails.
6. When temperature returns to normal:
   - System resets and continues monitoring.

---

## 🌐 Arduino Email Notification Process

- WiFi connection established
- Secure HTTPS client created
- JSON payload generated
- Data sent to Cloud Email API
- Email delivered to registered address

---

## 🔐 Key Features

✔ Real-time temperature monitoring  
✔ Secure HTTPS communication  
✔ Cloud-based Email Notification API  
✔ Event-based alert triggering  
✔ Prevents duplicate alerts  
✔ Easy IoT integration  

---

## 📄 Important Code Sections

### Include Required Libraries
```cpp
#include <WiFiS3.h>
#include <DHT.h>
#define DHTPIN 2
#define DHTTYPE DHT11
```

### Threshold Configuration
```cpp
const float TEMP_THRESHOLD = 30.0;
```

### Email Trigger Logic
```cpp
if (temperature > TEMP_THRESHOLD) {
  sendEmail(temperature, humidity);
}
```

---

## 📬 Applications

- Industrial Temperature Monitoring  
- Server Room Safety System  
- Home Automation Alerts  
- Cold Storage Monitoring  
- Smart Agriculture  
- IoT Training & Educational Projects  

---

## 🔧 Troubleshooting

### WiFi Not Connecting
- Verify SSID and password
- Check signal strength
- Monitor serial output

### DHT11 Not Giving Readings
- Check wiring
- Ensure correct sensor type
- Avoid long wires

### Email Not Received
- Verify API key and template ID
- Check HTTPS connection
- Check spam folder

### Multiple Email Alerts
- Ensure email flag logic is correct
- Verify retry delay setting

---

## 🔮 Future Enhancements

- Add multiple sensor support
- Add LCD/OLED display
- Add SMS or mobile push notifications
- Cloud dashboard integration
- Data logging & analytics

---

## 📚 Learning Outcomes

After completing this project, you will understand:

- Arduino WiFi communication
- Secure HTTPS requests
- JSON payload formatting
- Cloud API integration
- Event-based IoT notification systems

---

## 📌 Conclusion

This Real-Time Arduino Email Alert System demonstrates how environmental monitoring can be enhanced using cloud connectivity. By combining sensor data, WiFi communication, and secure email APIs, the system provides reliable and timely notifications.

The project is simple, scalable, and suitable for both beginners and real-world monitoring applications.

