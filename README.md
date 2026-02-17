# Quadrature Branch-Line Coupler Design & Analysis

This repository contains the electromagnetic design and performance verification of a **90-Degree Quadrature Branch-Line Coupler**. The project was simulated and validated using **Ansys Electronics Desktop (HFSS) 2025 R2 Student**.

## 🚀 Project Overview
The Branch-Line Coupler is a fundamental passive component used for power division and phase shifting in RF front-ends. It is designed to divide the input power equally between two output ports with a **90-degree phase difference**, while maintaining high isolation at the fourth port.

### Design Specifications:
- **Center Frequency:** 2.48 GHz
- **Substrate Material:** FR-4_epoxy (εr ≈ 4.4)
- **Port Impedance:** 50 Ohm matching
- **Topology:** Microstrip λ/4 branch sections

---

## 🛠 Design & Geometry
The coupler consists of four ports and four branch sections. The horizontal branches have a characteristic impedance of $Z_0/\sqrt{2} \approx 35.35 \, \Omega$, and the vertical branches match the system impedance $Z_0 = 50 \, \Omega$.


---

## 📊 Simulation Results

### 1. S-Parameters Analysis
The frequency response demonstrates precise tuning at the 2.48 GHz target:
- **S11 (Return Loss):** Exceptional matching achieved with **-46.61 dB** at **2.48 GHz**.
- **S21 & S31 (Power Division):** Equal power splitting verified near the -3 dB level.
- **S41 (Isolation):** High isolation confirmed, ensuring minimal leakage between input and isolated ports.

> **Technical Detail:** The deep null in $S_{11}$ (-46.61 dB) confirms that virtually no power is reflected, indicating a near-perfect impedance match at the center frequency.


### 2. Mesh & Solver Efficiency
The simulation was optimized for both accuracy and computational speed:
- **Max Solved Tetrahedra:** 2,936
- **Maximum Delta S:** 0.02 (Target reached within 6 passes)
- **Frequency Sweep Time:** **27 seconds**

---

## 🖥 Computational Setup
- **Solution Frequency:** 2.4 GHz (Single)
- **Adaptive Passes:** Maximum 6
- **Solver Type:** Driven Terminal

