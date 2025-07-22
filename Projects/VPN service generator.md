# Custom VPN Service like Tailscale

## 📝 Project Overview

A VPN server service inspired by Tailscale, aiming to provide secure peer-to-peer (P2P) connections using WireGuard, with login authentication, admin control, and file/RDP support.

---

## ✅ Phase 1: Core Features

- Secure encrypted tunnels using **WireGuard**
- **Username/password login** system (SQLite-based)
- **JWT-based session** management
- **Admin panel** to manage users and devices
- Devices appear on a **shared LAN** (LAN emulation)
- Support for **RDP** and **file sharing**
- **Local network only** for initial release (cross-network later)
- Cross-platform: **Windows, Linux, Android**
- **Python** as backend (Flask or FastAPI)

---

## 🧑‍💻 Tech Stack

- **Backend**: Python (Flask/FastAPI)
- **Database**: SQLite
- **Tunnel Protocol**: WireGuard
- **Authentication**: Username/Password + JWT
- **UI**: HTML/CSS/JS (optional dashboard UI)

---

## 🔐 Authentication & Authorization

- SQLite for storing user credentials
- JWT for session management
- Role-based access:
    - Admin: Full control, dashboard access
    - User: Tunnel-only access

---

## 🧩 WireGuard Integration (Python)

- Use `subprocess` to run WireGuard CLI commands (`wg`, `wg-quick`)
- Key generation handled via Python wrappers
- Write configuration files for interfaces
- Control tunnel start/stop from backend

---

## 🔁 Peer Discovery

- **Manual / local-only** device configuration for now
- No NAT traversal or central coordination yet
- Cross-network and relay (DERP-style) to be added in Phase 2

---
Here is the updated **Team Roles** section converted into a clean, organized table:

---

## 🧑‍🤝‍🧑 Team Roles (6 Members)

| Member   | Role                         | Responsibilities                                                           |
| -------- | ---------------------------- | -------------------------------------------------------------------------- |
| Member 1 | **Project Lead & Architect** | System architecture, planning, coordination                                |
| Member 2 | **Backend Developer**        | Implements login system, JWT-based session handling, admin panel APIs      |
| Member 3 | **WireGuard Engineer**       | Handles key generation, tunnel setup, interface scripting via Python       |
| Member 4 | **Client Device Support**    | Configures and tests client setup on Windows, Linux, and Android platforms |
| Member 5 | **UI/UX Developer**          | Builds admin dashboard UI, user-facing web views (if applicable)           |
| Member 6 | **Testing & Documentation**  | Performs QA, writes setup guides, README, and helps plan future features   |

---

Let me know if you'd like to include names, GitHub usernames, or assign backup roles too.
---

## 🔜 Future Features (Phase 2)

- Centralized control server for peer sync
- NAT traversal with STUN and relay servers (DERP)
- Multi-admin roles and ACLs
- OAuth or 2FA login
- Native Android app

---

## 🧠 P2P vs Centralized VPN Comparison

| Feature              | Peer-to-Peer (like Tailscale) | Centralized VPN (like OpenVPN)          |
| -------------------- | ----------------------------- | --------------------------------------- |
| **Performance**      | Fast, direct connection       | Slower, all traffic goes through server |
| **Server Load**      | Low (control server only)     | High (all traffic passes through)       |
| **NAT Traversal**    | Needs STUN/Relay (e.g., DERP) | Not needed                              |
| **Setup Complexity** | Moderate to High              | Low                                     |
| **Scalability**      | Very High                     | Limited by server hardware              |
| **Security**         | End-to-end with WireGuard     | TLS or WireGuard                        |

---

## 📦 Project Folder Structure (suggested)

```
vpn-project/
├── backend/
│   ├── app.py
│   ├── auth.py
│   ├── wg_utils.py
│   ├── database.sqlite
│   └── templates/
├── clients/
│   ├── linux_setup.sh
│   ├── windows_setup.bat
│   └── android_termux.md
├── static/
│   └── admin_dashboard.html
└── README.md
```

---

## 📌 Notes

- Focus on building and testing local tunnels first
- Future versions can enable remote connectivity, ACLs, and web-based coordination
- Modular approach allows each team member to work independently