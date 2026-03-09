This report is professionally structured for a GitHub repository. You can save this text as a `README.md` file in your project folder.

# Smart IoT Theft Detector with Alarm & Servo Lock

**Project Category:** IoT / Home Security

**Platform:** NodeMCU (ESP8266) & Blynk Cloud

**Contributors:** Tarush Chawla, Ujjwal Kumar Rai

---

## 📄 Project Overview

The **Smart IoT Theft Detector** is a low-cost, intelligent security solution designed to replace traditional, expensive alarm systems. By leveraging the **ESP8266 (NodeMCU)** and the **Blynk IoT platform**, this system provides real-time motion detection, remote access control, and physical security via a servo-controlled lock.

## 🚀 Key Features

* **Real-Time Intrusion Alerts:** Instant push notifications sent to your smartphone when motion is detected.
* **Remote Arm/Disarm:** Control the security state of your home from anywhere in the world via the Blynk app.
* **Dual-Layer Security:** * **Local:** High-decibel buzzer and LED visual alarm.
* **Physical:** Password-protected Servo Motor acting as a deadbolt/lock.


* **Bypass Mode:** Enter a secure password ("1234") in the mobile terminal to disarm the system and unlock the door for authorized entry.
* **Low Cost:** Built using affordable, off-the-shelf components.

## 🛠️ Hardware Components

| Component | Function |
| --- | --- |
| **NodeMCU (ESP8266)** | The "brain" with built-in Wi-Fi for cloud connectivity. |
| **PIR Sensor (HC-SR501)** | Detects infrared heat signatures from moving bodies. |
| **Servo Motor (SG90)** | Acts as the physical locking mechanism. |
| **Active Buzzer** | Produces a loud alarm during an intrusion. |
| **LED** | Provides a visual status indicator for the alarm. |
| **Jumper Wires & Breadboard** | For circuit connections and prototyping. |

## 💻 Software Stack

* **Arduino IDE:** Used for programming the NodeMCU in C++.
* **Blynk App (Legacy):** Provides the mobile dashboard for remote monitoring and control.
* **C++ Libraries:** `ESP8266WiFi.h`, `BlynkSimpleEsp8266.h`, and `Servo.h`.

## ⚙️ Working Logic

1. **Sensing:** The PIR sensor monitors the environment for motion.
2. **Verification:** If motion is detected, the NodeMCU checks if the system is "ARMED" via the Blynk cloud.
3. **Alerting:** If ARMED and motion occurs, the local buzzer/LED triggers, and a push notification is sent to the user's phone.
4. **Access Control:** The user can enter a password on the Blynk Terminal. If correct, the Servo rotates 90° to unlock the door and disables the alarm.

## 📈 Future Enhancements

* **ESP32-CAM Integration:** Capture and send photos of intruders to the user.
* **Blynk 2.0 Migration:** Update to the latest IoT standards for better data logging.
* **Battery Backup:** Implement LiPo battery support for protection during power outages.
* **Magnetic Reed Switches:** Add door/window contact sensors for 360-degree protection.

---

### How to Use

1. **Circuitry:** Connect the components as per the circuit diagram (available in the documentation).
2. **Configuration:** Replace the `Auth Token`, `SSID`, and `Password` in the provided code.
3. **Deployment:** Upload the code via Arduino IDE and set up the Blynk Dashboard with a Button (V1), Terminal (V2), and Notification widget.

---

*This project was developed as part of the ECE-282: IoT with NodeMCU course at Lovely Professional University.*
