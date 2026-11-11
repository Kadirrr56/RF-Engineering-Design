# 2.4 GHz Microstrip Parallel-Coupled Band-Pass Filter (BPF) Design and Optimization Report

**Prepared by:** Abdulkadir Oluç[cite: 11]
**Institution:** Muğla Sıtkı Koçman University, Electrical and Electronics Engineering[cite: 11]

### 1. Project Summary
This report presents the design, modeling, and optimization processes for a 3rd-order (N=3) Chebyshev-characteristic parallel-coupled microstrip band-pass filter, designed to operate within the 2.4 GHz ISM band[cite: 11]. The design and electromagnetic (EM) simulations were conducted using the CST Studio Suite environment; prior to the hardware prototyping phase, physical RF phenomena—such as dielectric losses and over-coupling—were analyzed to ensure the system was ready for fabrication[cite: 11].

### 2. Design Parameters and Material Properties
An FR4 substrate was selected for the design due to its cost-effectiveness and widespread availability[cite: 11]. Despite its lossy nature at high frequencies, transmission was maximized through geometric optimization[cite: 11].

| Parameter | Description | Value |
| :--- | :--- | :--- |
| **Substrate (FR4) Thickness (sub_h)** | Thickness of the dielectric material[cite: 11] | 1.6 mm[cite: 11] |
| **Copper Thickness (cu_h)** | Thickness of the conductive traces[cite: 11] | 0.035 mm[cite: 11] |
| **Resonator Length (L)** | Final resonator length after optimization[cite: 11] | 17.0 mm[cite: 11] |
| **Feed Line (W_feed)** | Width for 50-Ohm characteristic impedance[cite: 11] | 3.0 mm[cite: 11] |
| **Outer Section Width (W1)** | Width of the coupling line in the 1st and 4th sections[cite: 11] | 2.3 mm[cite: 11] |
| **Input Coupling Gap (S1)** | Initial signal jump distance[cite: 11] | 0.20 mm[cite: 11] |
| **Inner Section Width (W2)** | Width of the coupling line in the 2nd and 3rd sections[cite: 11] | 2.9 mm[cite: 11] |
| **Middle Coupling Gap (S2)** | Jump distance between the inner resonators[cite: 11] | 0.60 mm[cite: 11] |

### 3. Simulation and Optimization Process (Tuning)
Simulations were performed using the CST Time Domain Solver[cite: 11]. In the mesh settings, cell dimensions were carefully adjusted to capture the 0.035 mm thin copper profile; port boundary conditions were manually defined—with the reference plane set to the FR4 substrate (ground)—to account for fringing fields[cite: 11]. * **Iteration 1 (Theoretical Values):** High transmission loss (S21 = -55 dB) was observed with the initial values ​​(S2 = 1.20 mm)[cite: 11]. The signal failed to bridge the wide coupling gaps[cite: 11].
* **Iteration 2 (Over-coupling and Frequency Shift):** When the gaps were narrowed (S2 = 0.35 mm) and the resonator length was reduced (L = 16.3 mm), the transmission loss improved to -15 dB; however, the center frequency shifted to 2.65 GHz[cite: 11].
* **Final Optimization (Golden Ratio):** To balance the "pole splitting" effect and shift the resonance back to 2.4 GHz, the parameters were set to L = 17.0 mm and S2 = 0.60 mm, resulting in an optimal passband[cite: 11].

### 4. Simulation Results
The S-parameters of the final design met the following performance criteria[cite: 11]:

* **Return Loss (S11):** Consistent with a 3rd-order Chebyshev filter characteristic, "passband ripple" was observed within the passband[cite: 11]. The dual-dip structure (at -14 dB) occurring around 2.2 GHz and 2.65 GHz created a wide, stable band that effectively encompasses the 2.4 GHz center frequency[cite: 11]. * **Transmission Coefficient (S21):** Considering the lossy nature of the FR4 substrate, signal transmission has reached a stable plateau between -11 dB and -15 dB, approaching theoretical physical limits[cite: 11]. Successful signal transmission has been achieved[cite: 11].

> *(Note: Detailed visuals regarding the S11 Return Loss and S21 Transmission Coefficient simulation plots are available in the original Word document; please refer to that file.)*

### 5. Conclusion and Future Work
The electromagnetic modeling of the system has been successfully completed, and the targeted filtering characteristics for the 2.4 GHz ISM band have been achieved[cite: 11]. Principles of RF and high-frequency hardware have been practically verified using CST Studio Suite[cite: 11]. In the next phase, the design’s Gerber files will be exported for physical PCB fabrication, and S-parameter verification measurements will be conducted in a laboratory environment using a Vector Network Analyzer (VNA)[cite: 11].
