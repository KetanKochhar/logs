
# 🔐 Privacy Pendant – A Wearable Anti-Surveillance Device

## 🧠 Project Overview

The Privacy Pendant is a **wearable, low-cost device** designed to protect individuals from unauthorized surveillance. It uses **infrared LEDs** to disrupt hidden cameras and **ultrasonic frequencies** to jam nearby microphones.

This pendant is useful in environments where privacy is a concern — such as meetings, classrooms, interviews, and personal spaces.

---

## 🎯 Objectives

- Create a compact, wearable device to counter audio-visual spying.
- Emit IR rays to blind camera sensors.
- Emit ultrasonic noise (inaudible to humans) to interfere with microphone recordings.
- Keep the circuit simple and low-cost using basic electronic components.

---

## ⚙️ System Design

### 🔧 Hardware Components

| Component | Quantity | Function |
|----------|----------|----------|
| IR LEDs (850–940nm) | 4–6 | Blinds spy cameras |
| Ultrasonic Transducer (40kHz) | 1 | Jams hidden mics |
| Li-ion/Coin Cell Battery | 1 | Power supply |
| ON/OFF Switch | 1 | Manual control |
| Resistors | As needed | Current limiting |
| Breadboard/PCB | 1 | Circuit base |
| Ribbon/String | 1 | Wearable mounting |

---

### 🔌 Circuit Block Diagram

```

[ Battery ]  
|  
[ ON/OFF Switch ]  
|  
+--------+---------+  
| |  
[ IR LED Array ] [ Ultrasonic Buzzer ]

```

---

## 🧪 Testing

- Test IR LEDs using a smartphone camera in low light.
- Test ultrasonic jammer using a phone/voice recorder. Playback should show noise/distortion.
- Measure the effective jamming/blinding range.
  - IR Range: 0.5 to 1 meter
  - Mic Jam Range: 1 to 2 meters

---

## 🛠 Group Role Distribution (6-Member Team)

| Student | Role | Responsibilities |
|--------|------|------------------|
| **1. Circuit Designer** | Hardware Lead | Design and simulate circuit, select appropriate components |
| **2. Assembly Engineer** | Maker | Build the physical prototype (soldering/breadboard) |
| **3. Power Manager** | Power Systems | Choose batteries, manage voltage regulation, estimate battery life |
| **4. Test Engineer** | QA & Testing | Perform functional testing with phones/mics/cameras |
| **5. Research Analyst** | Documentation | Research privacy tech, document technical theory, assist in conclusion |
| **6. Presentation Lead** | PPT & Demo | Create slides, prepare demo, manage final presentation and team sync |

---

## 📈 Results

- Functional prototype built and tested successfully.
- Effective in blinding basic cameras and jamming nearby microphones in a ~1-meter range.
- Low-cost and wearable form factor achieved.

---

## 🚀 Future Scope

- Add auto-activation using motion or ambient sound detection
- Rechargeable battery with USB-C port
- Smart features (Bluetooth or mobile control)
- Miniaturized PCB and 3D-printed pendant shell

---

## 📚 References

- IR LED datasheets
- Ultrasonic transducer modules
- IEEE papers on acoustic jamming
- [Basic IR camera blinding experiment](https://www.instructables.com/How-to-Blind-CCTV-Cameras/)

---

## 🏁 Conclusion

This project demonstrates a practical solution to growing privacy concerns. The Privacy Pendant serves as a personal defense tool against electronic surveillance while staying simple, affordable, and effective for real-world use.

