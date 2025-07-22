# 🌐 Web-Based DNS Filtering System using ESP32

## 🎯 Project Overview

This project is a **web-based DNS filtering system** built using an **ESP32 microcontroller**. It is designed for **internal company or college networks** to **block unwanted websites**, **log DNS traffic**, and **monitor usage** — all through a **simple admin web dashboard**.

---

## 🧠 What is DNS?

DNS (Domain Name System) is like the internet’s phonebook. It translates human-readable domain names like `google.com` into IP addresses like `142.250.190.14`.

In this project, the ESP32 acts as a **custom DNS server** that:
- Allows or blocks certain domain requests
- Monitors what websites users are visiting
- Logs DNS activity to the cloud
- Can be controlled using a secure web dashboard

---

## 🧩 Key Features

| Feature                     | Description |
|----------------------------|-------------|
| ✅ Full DNS Server          | ESP32 listens on port 53 and responds to DNS requests |
| 🔒 Domain Blocking          | Blocks domains manually added by the admin |
| 🔍 Keyword Filtering        | Blocks domains containing specific words like `ads`, `track` |
| 👨‍💻 Per-Device Filtering     | Set rules based on IP or MAC address |
| ⏰ Time-Based Filtering      | Block specific domains at certain times of day |
| 📊 DNS Logging              | Logs all DNS queries to the cloud for review |
| 🌐 Web Dashboard (Admin UI) | Manage blocklists, view logs, and control rules |
| 🔐 Secure Login             | Admin-only access using username/password |
| ☁️ Cloud-Based Storage      | Blocklists, rules, and logs are stored in the cloud |
| 🔁 Real Device Testing      | Tested with phones, laptops on a real Wi-Fi/LAN network |

---

## 🛠️ System Components

### 1. **ESP32 Microcontroller**
- Runs the DNS server
- Applies filters and logs queries
- Communicates with the cloud via HTTP

### 2. **Web Dashboard**
- Admin panel to manage all settings
- Built using HTML + JS (e.g., React or plain HTML)
- Protected by login

### 3. **Cloud Backend**
- REST API to store and retrieve:
  - Blocklists
  - Logs
  - Device rules
  - Configurations
- Hosted using services like Render, Firebase, or locally

---

## 🔄 How It Works (Step-by-Step)

1. A device (like a laptop) sends a DNS query (e.g., `youtube.com`)
2. ESP32 receives the query and:
   - Checks blocklists, keywords, time, and device rules
   - If blocked → responds with error (`NXDOMAIN`)
   - If allowed → forwards to upstream DNS (e.g., `8.8.8.8`) and returns the real IP
3. The ESP32 logs the query (domain, time, device) and uploads to the cloud
4. Admin can view and update rules through the web dashboard

---

## 📡 Network Setup

- ESP32 is connected to the network via **Wi-Fi or Ethernet**
- Test devices (laptop, phone) are manually configured to use **ESP32 as their DNS server**
- ESP32 forwards allowed requests to a public DNS (like Google DNS)

---

## 🔐 Communication

| Between       | Method | Description |
|---------------|--------|-------------|
| ESP32 → Cloud | HTTP   | Sends logs, fetches filters |
| Web UI → Cloud | HTTP  | Admin controls filters and views logs |
| ESP32 → Devices | DNS  | Responds to DNS queries directly |

---

## 🧪 Testing Plan

- Use 3–5 test devices (phones, laptops)
- Set their DNS manually to ESP32’s IP
- Try visiting both allowed and blocked sites
- Monitor log accuracy in the web dashboard
- Test time-based rules and keyword blocking
- Simulate admin actions (add/remove block entries)

---

## 🗃️ Example Cloud API Endpoints

| Endpoint                  | Method | Description |
|---------------------------|--------|-------------|
| `/api/blocklist`          | GET    | ESP32 fetches blocklist |
| `/api/logs`               | POST   | ESP32 uploads logs |
| `/api/device-rules/{mac}` | GET    | Device-specific rules |
| `/api/login`              | POST   | Admin login |
| `/api/settings`           | GET    | General DNS config |

---

## 🔧 Tools & Libraries

| Component     | Tool/Library                              |
| ------------- | ----------------------------------------- |
| ESP32 Code    | Arduino or ESP-IDF, AsyncUDP, ArduinoJson |
| Cloud Backend | Node.js, Flask, or FastAPI                |
| Database      | Firebase, MongoDB, or PostgreSQL          |
| Frontend      | React.js, HTML + CSS + JS                 |
| Hosting       | Vercel, Render, or localhost              |

---
Perfect — with **6 students**, you have the ideal team size to fully distribute the work while allowing each person to specialize.

Here’s a clear role-based breakdown, tasks per member, and how they’ll collaborate efficiently.

---

## 👥 **6-Member Team Structure**

| Member | Role                                     | Responsibilities                                                                                                                                  |
| ------ | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🧠 A   | **Team Leader & System Architect**       | - Plan overall architecture- Coordinate between all sub-teams- Track progress and testing- Final integration of system                            |
| 🧲 B   | **Embedded Systems Developer (ESP32)**   | - Program DNS server on ESP32- Handle domain parsing, filtering, and forwarding- Communicate with cloud API using HTTP                            |
| 🧩 C   | **Backend Developer (API & DB)**         | - Build REST API with login, blocklists, logs, etc.- Design cloud database structure- Ensure ESP32 can fetch/post data                            |
| 🌐 D   | **Frontend Developer (Admin Dashboard)** | - Design & build web dashboard- Create pages for login, logs, filtering, etc.- Connect UI to backend API                                          |
| ☁️ E   | **Cloud & Deployment Engineer**          | - Deploy backend & frontend on a platform (e.g., Vercel, Render, Firebase)- Setup database & cloud security- Configure domain & HTTPS (if needed) |
| 🧪 F   | **Testing & Documentation Lead**         | - Run tests with real devices- Create testing scripts (block/allow cases)- Write final project report, user manual, screenshots, diagrams         |

