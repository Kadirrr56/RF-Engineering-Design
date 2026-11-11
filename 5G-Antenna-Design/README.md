# Report on the Design of a 28 GHz Microstrip Patch Antenna and 1x2 Array for 5G Communication Systems

**Prepared by:** Abdulkadir Oluç[cite: 12]
**Institution:** Muğla Sıtkı Koçman University, Department of Electrical and Electronics Engineering[cite: 12]

### 1. Project Parameters and Objectives
This project involves the design of a microstrip patch antenna and a 1x2 antenna array operating at a center frequency of 28 GHz, intended for use in 5G and 6G communication systems[cite: 12]. The low-loss substrate material Rogers RT/duroid 5880 was utilized throughout the design process[cite: 12].

**Key Parameters:**
* **Center Frequency (fr):** 28 GHz[cite: 12]
* **Substrate:** Rogers RT/duroid 5880 (εr = 2.2, tanδ = 0.0009)[cite: 12]
* **Substrate Thickness (h):** 0.254 mm[cite: 12]

### 2. Single Patch Antenna Design and Optimization
An "Inset Feed" technique was applied to maximize antenna impedance matching[cite: 12]. During the design phase, the patch and the feed line were kept as separate entities within the CST Studio workspace; they were not merged using a "Boolean Add" operation, in order to preserve the structural integrity of the model[cite: 12].

**Dimensions:**
* **Patch Width (W):** 4.24 mm | **Patch Length (L):** 3.47 mm[cite: 12]
* **Feed Line Width (Wf):** 0.79 mm | **Inset Length (Fi):** 1.05 mm | **Gap (G):** 0.4 mm[cite: 12]

#### 2.1. Single Antenna Simulation Results
The antenna exhibits an excellent resonance at exactly 28 GHz, with an S11 value of approximately -19 dB[cite: 12]. An examination of the 3D radiation pattern (far-field) confirms that the single patch antenna produces a clean radiation profile along the Z-axis (broadside), with a maximum gain of 7.58 dBi[cite: 12].

> *(Note: The S11 plot and 3D radiation pattern (far-field) images are available in the original Word document; please refer to that file.)*

### 3. 1x2 Antenna Array Design
To achieve beam steering and increased gain, a 1x2 array structure was created by replicating the single antenna element[cite: 12]. The spacing between the antennas was set to half a wavelength (λ0/2 = 5.35 mm) to minimize mutual coupling and suppress unwanted grating lobes[cite: 12].

> *(Note: The image showing the 1x2 array design in CST Studio Suite and the port feed coordinates is available in the Word document; please refer to that file.)*

#### 3.1. Array S-Parameter Analysis
The return losses (S11 and S22) for Port 1 (left antenna) and Port 2 (right antenna) exhibit resonance symmetrically at approximately -19 dB at 28 GHz [cite: 12]. Furthermore, the S21 (mutual coupling) value remains at approximately -14 dB, confirming that the isolation between the antennas is at an adequate level [cite: 12].

> *(Note: The plots for Port 1 S11, Port 2 S22, and S21 isolation/coupling are available in the Word document; please refer to them there.)*

#### 3.2. Array 3D Radiation Pattern
It has been confirmed that, when both ports of the 1x2 array structure are excited, the beam becomes narrower compared to that of a single antenna, and the maximum gain increases to 7.63 dBi (indicating enhanced directivity due to the combined effect) [cite: 12].

> *(Note: The 3D radiation pattern (far-field) for the array structure is available in the Word document; please refer to it there.)*

### 4. Conclusion
The simulations demonstrate that both the single patch antenna and the 1x2 antenna array successfully meet the target values ​​for electrical and radiation performance—namely, excellent impedance matching, sufficient isolation, and high gain—within the 28 GHz 5G frequency band [cite: 12]. ---

### Appendix 1: Mathematical Calculations for the 28 GHz Microstrip Patch Antenna
The theoretical calculations for the Rogers RT/duroid 5880 substrate (εr = 2.2, h = 0.254 mm) used in the design are provided below[cite: 12]:

**1. Calculation of Patch Width (W)**
* W = (c / 2fr) * √[2 / (εr + 1)][cite: 12]
* W = 5.357 mm * 0.7905 = 4.235 mm[cite: 12]

**2. Determination of Effective Dielectric Constant (εreff)**
* εreff = ((εr + 1) / 2) + ((εr - 1) / 2) * [1 + 12(h / W)]^(-1/2)[cite: 12]
* εreff = 1.6 + 0.6 * 0.762 = 2.057[cite: 12]

**3. Calculation of Effective Length (Leff)**
* Leff = c / (2fr * √(εreff))[cite: 12]
* Leff = (3 * 10^8) / (2 * 28 * 10^9 * 1.434) = 3.73 mm[cite: 12]

**4. **Determination of the Length Extension (ΔL)**
* ΔL = 0.412 * h * [((εreff + 0.3)(W/h + 0.264)) / ((εreff - 0.258)(W/h + 0.8))][cite: 12]
* ΔL = 0.412 * 0.254 * 1.27 = 0.133 mm[cite: 12]

**5. Calculation of the Actual Physical Length (L)**
* L = Leff - 2ΔL[cite: 12]
* L = 3.73 - 2(0.133) = 3.464 mm[cite: 12]

*Consequently, the values ​​obtained via the formulas—W = 4.235 mm and L = 3.464 mm—were refined through further optimization within the simulation environment, resulting in final values ​​of W = 4.24 mm and L = 3.47 mm[cite: 12].*
