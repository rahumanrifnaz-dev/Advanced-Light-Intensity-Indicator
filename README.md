# Advanced Light Intensity Indicator (ALII)

An innovative, purely hardware-based digital logic solution designed to monitor, stabilize, and average ambient light intensity levels to promote energy conservation and smarter city lighting.

**Institution:** University of Moratuwa  
**Program:** B.Sc. Engineering (Honours) in Electrical Engineering

---

## 📖 Project Overview

The **Advanced Light Intensity Indicator (ALII)** module provides real-time information about ambient light intensity to support the efficient use of artificial lighting systems.

By identifying when natural light is sufficient, the system can be used to support the dimming or switching off of artificial lights, helping reduce unnecessary energy consumption. The concept also has potential applications in **smart city lighting** and **self-sustaining solar-powered systems**.

The project was designed and implemented using **discrete logic gates and flip-flops**, without programmable microcontrollers or pre-built task-specific ICs. This demonstrates fundamental concepts in **digital electronics, analog signal conditioning, analog-to-digital conversion, timing, stability detection, and digital signal processing**.

---

## ✨ Key Features

### 1. Analog Noise Filtering

An analog filtering stage is implemented before the LDR signal enters the digital processing section.

- Reduces unwanted electrical noise.
- Suppresses approximately **50–100 Hz power-line interference**.
- Reduces unstable readings and flickering caused by electrical noise.
- Allows genuine ambient light variations to be processed more reliably.

### 2. Discrete Logic ADC & Display

The system uses an **LDR (Light Dependent Resistor)** to sense ambient light intensity.

The sensor output is converted into discrete digital intensity levels using a custom **flash ADC-based logic structure**.

The resulting intensity level is displayed using a **7-segment display**:

- `0` → Lowest light intensity
- `7` → Highest light intensity

### 3. Adjustable Stability Detector

The stability detector prevents temporary light fluctuations from immediately changing the displayed output.

For example, temporary shadows caused by a person walking past the sensor can be ignored if the signal does not remain stable for the required period.

**Features:**

- Adjustable stability period: **30–300 seconds**
- Variable-resistor-based adjustment
- Prevents false or unnecessary output changes
- Optional bypass switch to enable/disable the stability function

### 4. Moving Average Calculator

A second 7-segment display provides the **average light intensity over a rolling time period**.

**Features:**

- Adjustable averaging period: **300–900 seconds**
- Stores and processes previous intensity measurements
- Displays the calculated average intensity
- Dedicated push-button for resetting the stored average

---

## 🛠️ Hardware & Logic Constraints

The project was intentionally designed under strict hardware-based digital logic constraints.

| Category | Implementation |
|---|---|
| Sensor | LDR (Light Dependent Resistor) |
| Analog Processing | Analog filtering and signal conditioning |
| ADC | Custom flash ADC-based logic |
| Digital Logic | Standard logic gate ICs |
| Memory / Timing | Flip-flops and discrete logic |
| Display | 7-segment displays |
| Stability Control | Discrete timing and logic circuitry |
| Averaging | Discrete digital logic |
| Microcontrollers | **Not used** |
| Programmable ICs | **Not used** |
| Task-specific ICs | **Not used** |

---

## ⚙️ System Concept

The overall signal-processing sequence can be represented as:

```text
Ambient Light
      ↓
     LDR
      ↓
Analog Signal Conditioning
      ↓
Noise Filtering
      ↓
Flash ADC / Comparator Logic
      ↓
Digital Light Intensity Level
      ↓
 ┌───────────────────────┐
 │                       │
 ↓                       ↓
Stability Detector    Moving Average
 │                       │
 ↓                       ↓
Current Level        Average Level
 │                       │
 └──────────┬────────────┘
            ↓
       7-Segment Displays
```

---

## 📸 Visuals

### Physical Hardware Implementation

The physical ALII circuit was implemented using breadboards. The hardware demonstrates the power distribution, analog filtering stage, digital logic circuitry, and dual 7-segment displays used for real-time and averaged light-intensity outputs.

![Hardware Setup](<images/WhatsApp Image 2026-08-21 at 14.25.34.jpeg>)

### Logic Simulation

The complete circuit was modeled and tested in a simulation environment. The simulation includes the Flash ADC, Stability Detector, and Moving Average Calculator subsystems.

![Simulation Circuit](<images/WhatsApp Image 2026-08-21 at 10.33.01.jpeg>)

### Project Team Demo

Demonstration of the working ALII hardware module together with the corresponding software simulation.

![Team Demo](<images/WhatsApp Image 2026-08-11 at 21.57.01 (2).jpeg>)
## 📂 Repository Contents

```text
.
├── README.md
├── docs/
│   └── ALII_Project_Report.pdf
├── src/
│   └── simulation/
├── media/
└── images/
    ├── hardware_setup.jpeg
    ├── simulation_logic.jpeg
    └── team_demo.jpeg
```

### `/docs`

Contains the complete project report, including:

- Project objectives
- System architecture
- Design methodology
- Circuit design decisions
- Assumptions
- Component selection
- Detailed circuit explanations
- Testing and results

### `/src/simulation`

Contains the simulation files used to design and verify the digital logic and system operation.

### `/media`

Contains demonstration media, including screen recordings showing the working features of the simulation.

### `/images`

Contains project photographs and simulation screenshots used in this README.

---

## 🎯 Project Objectives

The main objectives of the ALII project are to:

1. Develop a hardware-based light-intensity monitoring system.
2. Convert an analog LDR signal into discrete digital intensity levels.
3. Demonstrate ADC operation using discrete logic.
4. Reduce the effect of electrical noise on sensor measurements.
5. Prevent false output changes caused by temporary light fluctuations.
6. Implement a configurable stability-detection mechanism.
7. Calculate and display the average light intensity over a configurable period.
8. Demonstrate digital electronics concepts without using programmable microcontrollers.
9. Explore potential applications in energy-efficient and smart lighting systems.

---

## 🌱 Potential Applications

The ALII concept can be extended to applications such as:

- Smart street lighting
- Energy-efficient building lighting
- Automated indoor lighting
- Solar-powered lighting systems
- Smart-city infrastructure
- Ambient-light monitoring systems
- Energy conservation systems

---

## 🧠 Engineering Concepts Demonstrated

This project combines several electrical and electronics engineering concepts:

- LDR-based sensing
- Analog signal conditioning
- Low-pass / notch filtering
- Noise suppression
- Comparator circuits
- Flash ADC architecture
- Digital logic design
- Flip-flop-based memory
- Timing circuits
- Stability detection
- Moving-average processing
- 7-segment display interfacing
- Hardware-based signal processing

---

## 👥 Contributors

| Name | Student ID |
|---|---|
| **Ranasingha R.A.T.U** | 230519F |
| **Ranaweera R.K.D.H.M** | 230529K |
| **Ranmuthu S.G** | 230532M |
| **Rashmika R.P.P** | 230538L |
| **Rifnaz K.R.M** | 230550P |
| **Rodrigo B.K.G.S** | 230551U |

---

## 🎓 Academic Context

**University:** University of Moratuwa, Sri Lanka  
**Degree:** B.Sc. Engineering (Honours) in Electrical Engineering  
**Project:** Advanced Light Intensity Indicator (ALII)

---

## 📜 License

This project was developed as an academic engineering project at the **University of Moratuwa**.

Unless otherwise stated, the contents of this repository are intended for **academic and educational purposes**.
