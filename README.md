# MOCAP-NODE-V1

An open-source, ultra-compact (35 x 35 mm) wireless motion-capture (MoCap) node designed for body-worn biomechanical tracking. Built around an **ESP32-C3 Mini** and a 9-axis **Bosch BNO055** IMU, this platform is engineered for low-latency, peer-to-peer orientation streaming across multi-node clusters.

---

## Key Hardware Features

* **Core Processing & Wireless:** Powered by the **ESP32-C3 Mini** (RISC-V 32-bit single-core up to 160 MHz), running low-latency ESP-NOW peer-to-peer networking to sync 5 to 10 body-worn nodes without needing a Wi-Fi router.
* **9-Axis Motion Sensing:** Onboard **Bosch BNO055** smart IMU running hardware sensor fusion to directly output absolute orientation (Quaternions and Euler angles) for accurate limb and body tracking.
* **Power Management:** Integrated 1S (single-cell) LiPo battery charger with automatic power-path management for completely untethered wireless operation.
* **Wearable Form Factor:** Ultra-compact 35 x 35 mm footprint tailored for mounting on body straps (limbs, torso, head) without restricting natural human movement.
* **Peripherals:** USB Type-C connectivity for programming, debugging, and battery charging alongside status diagnostic LEDs.

---

## PCB Layer Architecture

Designed in **Altium Designer**, the PCB utilizes a dense, optimized 4-layer stack-up to ensure signal integrity, clean power distribution, and minimal interference for wireless RF and analog sensor lines:

| Layer | Designation | Description |
| :--- | :--- | :--- |
| **L1** | `SIG` | Primary Component Placement & Top Signal Routing |
| **L2** | `GND` | Solid Internal Ground Plane for EMI & RF Shielding |
| **L3** | `PWR` | Dedicated Internal Power Distribution Plane (3.3V / VBAT / VBUS) |
| **L4** | `SIG + GND` | Bottom Signal Routing & Secondary Ground Pour |

### Layer Previews

<details>
<summary><b>Click to expand layer views</b></summary>

* **L1 (SIG):**  
  <img width="100%" alt="L1 SIG" src="PASTE_YOUR_IMAGE_LINK_HERE" />

* **L2 (GND):**  
  <img width="100%" alt="L2 GND" src="PASTE_YOUR_IMAGE_LINK_HERE" />

* **L3 (PWR):**  
  <img width="100%" alt="L3 PWR" src="PASTE_YOUR_IMAGE_LINK_HERE" />

* **L4 (SIG + GND):**  
  <img width="100%" alt="L4 SIG+GND" src="PASTE_YOUR_IMAGE_LINK_HERE" />

</details>

---

## 3D PCB Rendering

<p align="center">
  <img width="100%" alt="3D View" src="PASTE_YOUR_IMAGE_LINK_HERE" />
</p>

---

## Repository Structure

```text
├── Altium/               # Schematic & 4-layer PCB layout project files
├── Firmware/             # ESP-IDF / Arduino source code and ESP-NOW sync drivers
├── Fabrication/          # Gerber files, BOM, and pick-and-place data
└── README.md             # Project documentation
