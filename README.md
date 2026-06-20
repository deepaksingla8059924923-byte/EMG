# EMG Acquisition Board

A compact, battery-powered, high-resolution **electromyography (EMG)** acquisition system designed for biosignal recording, wireless streaming, and onboard data logging.

---

## Features

- Battery-powered operation (**3–6 V DC only**)
- High-resolution **24-bit EMG acquisition**
- Wireless communication via **Bluetooth Low Energy (BLE)**
- Onboard **microSD card logging**
- Integrated **3-axis accelerometer** for motion tracking
- Low-noise analog power rails (**+2.5 V / −2.5 V**)
- Compact octagonal PCB form factor

---

## Hardware Specifications

| Parameter | Specification |
|------------|----------------|
| **Microcontroller** | PIC32MX250F128B with chipKIT UDB32-MX2-DIP bootloader |
| **Analog Front End** | ADS1299 (24-bit ADC) |
| **Accelerometer** | LIS3DH (3-axis) |
| **Wireless Connectivity** | RFduino BLE |
| **Storage** | microSD card slot |
| **Input Power** | 3–6 V DC battery only |
| **Input Voltage Range** | ±2.5 V |
| **Signal-to-Noise Ratio (SNR)** | 121 dB |
| **Power Rails** | +3.3 V, +2.5 V, −2.5 V |
| **Board Dimensions** | 2.41" × 2.41" octagon (1" edge length) |
| **Mounting Holes** | 1/16" ID, 0.8" × 2.166" center-to-center |

---

## Bill of Materials (BOM)

- PIC32MX250F128B Microcontroller
- ADS1299 Analog Front End
- LIS3DH 3-Axis Accelerometer
- RFduino BLE Module
- microSD Card Socket
- +3.3 V Voltage Regulator
- +2.5 V Analog Regulator
- −2.5 V Analog Regulator

---

## ADC Resolution

The ADS1299 features a **24-bit analog-to-digital converter (ADC)**:

```math
2^{24} = 16,777,216
```

Theoretical voltage resolution:

```math
\text{Resolution} = \frac{\text{Voltage Range}}{2^{24}}
```

Assuming a 5 V full-scale range:

```math
\frac{5\ \text{V}}{16,777,216} \approx 0.298\ \mu\text{V/bit}
```

> **Note:** Actual effective resolution depends on the ADS1299 reference voltage, PGA gain settings, and system noise.

---

## Applications

- Surface EMG (sEMG)
- Human–Machine Interfaces (HMI)
- Prosthetic Control
- Gesture Recognition
- Rehabilitation Monitoring
- Biomechanical Analysis
- Research and Education

---

## Power Requirements

> **Important:** Use battery power only during signal acquisition to minimize electrical noise.

- Input voltage: **3–6 V DC**
- Recommended source: **Li-ion/LiPo battery**
- USB power is not recommended during EMG recording

---
