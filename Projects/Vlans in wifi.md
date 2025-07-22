# VLAN-Based User Segregation in Wi-Fi using ESP32

## 📌 Project Title
**Dynamic VLAN Assignment Over Wi-Fi Using ESP32 with LAN8720 Ethernet Bridge**

---

## 📖 Abstract

This project demonstrates a practical approach to network segmentation using Virtual LANs (VLANs) based on user authentication. The system uses an **ESP32** microcontroller in **SoftAP mode** to serve as a captive Wi-Fi access point. After login, users are dynamically assigned to a VLAN by an external server. The ESP32 communicates via Ethernet (LAN8720 module) with a **VLAN-capable router**, enabling real VLAN routing and isolation across the network.

---

## 🎯 Objectives

- Authenticate users on Wi-Fi using a captive portal.
- Assign IP and VLAN dynamically based on user credentials.
- Simulate real enterprise network behavior using open-source and embedded systems.
- Understand and implement basic networking and Layer 2 segmentation using ESP32 and VLAN-capable routers.

---

## 🧰 Hardware Components

| Component              | Quantity | Description                                  |
|------------------------|----------|----------------------------------------------|
| ESP32 Dev Module       | 1        | Runs the Wi-Fi AP and captive portal         |
| LAN8720 Ethernet Module| 1        | Adds Ethernet capability to ESP32            |
| External Server (Laptop/RPi) | 1   | Handles authentication + VLAN mapping logic  |
| VLAN-Capable Router    | 1        | e.g., TP-Link TL-R605, MikroTik hEX, etc.    |
| Breadboard, Wires, PSU | -        | For connectivity and prototyping             |

---

## 🧠 Software Stack

- **ESP32 (Arduino / ESP-IDF)**
- **LAN8720 Driver + Ethernet stack**
- **Node.js / Python Flask** (Authentication Server)
- **Router Configuration Interface** (Manual VLAN setup)
- **Wireshark / Nmap** (Optional for testing VLAN traffic)

---

## 🔁 Working Flow

1. **ESP32 (SoftAP Mode)**  
   - Hosts Wi-Fi SSID for users.
   - Captive portal redirects users to login page.

2. **User Login**  
   - Enters username/password via captive portal.
   - ESP32 sends credentials to external server.

3. **External Server Response**  
   - Validates user.
   - Returns assigned VLAN ID and IP range.

4. **ESP32 VLAN Request Forwarding**  
   - Routes user through Ethernet to correct VLAN based on server instruction.
   - VLAN-capable router performs final VLAN assignment.

5. **Network Segregation Achieved**  
   - Each user is isolated in their VLAN.
   - Access control can be applied per VLAN.

---

## 🧪 Example VLAN Mapping

| Username | VLAN ID | Subnet          | Description           |
|----------|---------|------------------|------------------------|
| student1 | VLAN 10 | 192.168.10.0/24 | Internet + Lab Access |
| staff1   | VLAN 20 | 192.168.20.0/24 | Full Access            |
| guest1   | VLAN 30 | 192.168.30.0/24 | Limited Internet Only |

---

## 🔒 Security & Isolation

- Users in different VLANs cannot ping or access each other.
- Each VLAN can be controlled via router ACLs (Access Control Lists).
- Passwords and IP assignment controlled centrally via secure server logic.

---

## 👥 Team Roles (6 Members)

| Name     | Role                                            |
| -------- | ----------------------------------------------- |
| Member 1 | ESP32 Programming (Wi-Fi + Captive Portal)      |
| Member 2 | LAN8720 + Ethernet Integration                  |
| Member 3 | External Server & API (Auth + VLAN map)         |
| Member 4 | Router VLAN Setup & Networking                  |
| Member 5 | UI/UX for Captive Portal                        |
| Member 6 | Documentation + Testing (Ping, Wireshark, etc.) |

---

## 📷 Optional Enhancements

- MAC address-based filtering
- Logging user access attempts
- Admin dashboard for managing VLAN mappings
- Rate-limiting or time-based Wi-Fi access
- Integration with RADIUS or LDAP

---

## 📎 References

- [ESP32 with Ethernet (LAN8720)](https://randomnerdtutorials.com/esp32-ethernet-lan8720/)
- [802.1Q VLAN Basics](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/lanswitch/configuration/xe-3s/lanswitch-xe-3s-book/lanswitch-vlan.html)
- [TP-Link TL-R605 VLAN Config](https://www.tp-link.com/in/support/faq/2953/)
- [ESP-IDF Docs](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/)
