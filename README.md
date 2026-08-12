# MICROMOUSE-V2

An open-source, high-performance autonomous Micromouse platform engineered for competitive maze-solving. Built around a high-speed **STM32F405RGT6** core, this platform is optimized for rapid acceleration, sub-millimeter positioning accuracy, and real-time wall-sensing algorithms.

---

## Key Hardware Features

* **Core Processing:** Powered by the **STM32F405RGT6** (ARM Cortex-M4 running at 168 MHz with 1MB Flash and 192KB RAM) executing high-speed maze-solving and closed-loop motor control algorithms.
* **Optical Sensing:** 5 discrete IR sensors configured for precise wall detection, distance mapping, and real-time centering.
* **Precision Odometry:** Dual magnetic encoder PCBs engineered to break away from the main board and mount directly onto wheel shafts for tight closed-loop feedback.
* **Actuation System:** Dual discrete motor drivers tailored for responsive coreless and micro-dc motor management.
* **Power Management:** Integrated reverse-polarity battery protection paired with an efficient step-down conversion circuit for stable logic power delivery.
* **Peripherals & Debugging:** Onboard USB connectivity for high-speed logging and flashing, user-assignable buttons, and diagnostic status LEDs.

---

## PCB Layer Architecture

Designed in **Altium Designer**, the 4-layer PCB features a high-density layout optimized for signal integrity, minimal ground bounce, and clean power distribution:

| Layer | Designation | Description |
| :--- | :--- | :--- |
| **L1** | `SIG` | Primary Component Placement & Top Signal Routing |
| **L2** | `GND` | Solid Internal Ground Plane for EMI Shielding & Return Paths |
| **L3** | `PWR` | Dedicated Internal Power Distribution Plane |
| **L4** | `SIG + GND` | Bottom Signal Routing & Secondary Ground Pour |

### Layer Previews

<details>
<summary><b>Click to expand layer views</b></summary>

* **L1 (SIG):**  
  <img width="100%" alt="L1 SIG" src="https://github.com/user-attachments/assets/b8c8f218-e328-44df-8001-f4d3a7ccfeab" />

* **L2 (GND):**  
  <img width="100%" alt="L2 GND" src="https://github.com/user-attachments/assets/e4a734b8-dea2-48d9-a056-546f5d2985f7" />

* **L3 (PWR):**  
  <img width="100%" alt="L3 PWR" src="https://github.com/user-attachments/assets/49537f79-96bf-4cfc-a1e3-ba3ef9e25abb" />

* **L4 (SIG + GND):**  
  <img width="100%" alt="L4 SIG+GND" src="https://github.com/user-attachments/assets/e3f815d3-db63-4863-9e2a-76b76b9e1210" />

</details>

---

## 3D PCB Rendering

<p align="center">
  <img width="100%" alt="3D View" src="https://github.com/user-attachments/assets/591966c6-bb13-4303-9dbd-e98803343782" />
</p>

---

## Repository Structure

```text
├── Altium/               # Schematic & PCB layout project files
├── Firmware/             # STM32 source code and maze-solving algorithms
├── Fabrication/          # Gerber files, BOM, and pick-and-place data
└── README.md             # Project documentation
