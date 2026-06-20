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
| **Analog Front End** | ADS1299IPAG (24-bit ADC) |
| **Accelerometer** | LIS3DHTR (3-axis) |
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

| Component | Manufacturer Part Number | Unit Price (INR) | Notes |
|------------|--------------------------|-----------------:|-------|
| Microcontroller | PIC32MX250F128B-I/SP | ₹481.74 | 28-SPDIP package |
| Analog Front End | ADS1299IPAG | ₹9,484.08 | 8-channel, 24-bit AFE |
| Accelerometer | LIS3DHTR | ₹183.35 | 3-axis MEMS accelerometer |
| BLE Module | RFduino RFD22102 | N/A | Retired / no longer available |
| microSD Card Socket | 112J-TDAR-R01 | ₹116.25 | microSD connector only |
| +3.3 V Regulator | TPS7A2033PDBVR | ₹33.08 | Low-noise LDO |
| +2.5 V Regulator | TPS7A2025PDBVR | ₹32.61 | Low-noise LDO |
| −2.5 V Inverter | TPS60403DBVR | ₹109.02 | Charge-pump inverter |
| Passive Components | Resistors, capacitors, ESD parts | ₹200–₹500 | Estimated |
| PCB Fabrication | 2.41" × 2.41" custom PCB | ₹500–₹1,500 | Estimated, depends on quantity |

### Estimated Cost

| Category | Cost (INR) |
|-----------|-----------:|
| Core ICs + connectors + regulators | ₹10,440.13 |
| Passives + PCB fabrication | ₹700–₹2,000 |
| **Estimated prototype total** | **₹11,140–₹12,440** |

> RFduino is discontinued. If you are starting a new revision, replace it with a current BLE module instead of building around obsolete parts.

---

## ADC Resolution

The ADS1299 features a **24-bit analog-to-digital converter (ADC)**:

## CIRCUIT DIAGRAM
<img width="5037" height="3237" alt="image" src="https://github.com/user-attachments/assets/8a1592b6-d766-4f1d-a04e-07c9d3bd605f" />


```math
2^{24} = 16,777,216
