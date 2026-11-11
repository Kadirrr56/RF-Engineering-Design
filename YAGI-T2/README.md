# YAGI-T2: Design and Analysis Report for a 4-Element UHF Yagi-Uda Antenna

### Project Objective
The primary objective of this project is to perform theoretical calculations for a 4-element directional Yagi-Uda antenna designed for the UHF band (target center frequency: 600 MHz)—commonly used in DVB-T2 broadcasting systems—and to conduct 3D electromagnetic simulations using CST Studio Suite. The study specifically analyzes the physical effects of antenna element thickness (parasitic capacitance) on the resonance frequency.

### 1. Theoretical Design and Simulation Setup
The design is based on standard Balanis/Kraus coefficients, utilizing a 0.2λ spacing. Given the speed of light and a target frequency of 600 MHz, the wavelength (λ) is calculated to be 50 cm.

All antenna elements are modeled as 10 mm diameter cylinders (composed of PEC material), and the system is excited via a 75-ohm Discrete Port connected to the center of the driven dipole.

> *(Note: Graphics/figures illustrating the design geometry and the port feed point are available in the Word document for your reference.)*

### 2. S-Parameters (S11) and Frequency Shift Analysis
An S11 (Return Loss) analysis was conducted using the Time Domain Solver to evaluate the antenna's impedance matching and the efficiency of power radiation into free space. > *(Note: The S11 Return Loss plot and the results showing the resonance point at 565 MHz are available in the Word document; you may refer to them there.)*

* **Engineering Observation:** Although the theoretical calculations targeted 600 MHz, the simulation results show that the antenna achieves a highly effective resonance (-15.5 dB) at 565 MHz.
* **Root Cause Analysis:** Theoretical formulas are derived based on ideal, "zero-thickness" wires. In this design, the use of thick cylinders with a 10 mm diameter introduced parasitic capacitance into the system; this physical factor naturally caused the resonance frequency to shift downward (from 600 MHz to 565 MHz).

### 3. VSWR (Voltage Standing Wave Ratio) Analysis
VSWR values—another key indicator of impedance matching—have been evaluated.

> *(Note: The VSWR frequency characteristic plot is available in the Word document; you may refer to it there.)*

At 565 MHz, the frequency where the antenna reaches resonance, the VSWR value is observed to fall below 1.5 (approximately 1.4). This figure is well within the industry-standard limit of VSWR < 2, confirming that the power from the transmitter is being radiated successfully with minimal reflection.

### 4. Far-Field and Radiation Pattern
To examine the antenna's directivity—its ability to focus power in specific directions—3D far-field data has been analyzed. > *(Note: The results showing the 3D radiation pattern and directivity distribution at 580 MHz are available in the Word document; you may refer to them there.)*

* **Directivity:** 6.39 dBi
* **Analysis:** As expected from a Yagi-Uda design, the antenna exhibits a directional characteristic. The main lobe in the forward direction is clearly visible, and the gain value of 6.39 dBi falls within reasonable limits for a 4-element structure.

### 5. Conclusion
This simulation project has demonstrated that when theoretical calculations for RF designs are translated into practical models (which possess physical thickness), a frequency shift occurs. It was observed that shortening only the driven element (via parametric sweep) to shift the design to 600 MHz disrupts impedance matching; therefore, it was concluded that all physical dimensions within the system—including element lengths and the spacing between them—must be scaled proportionally (frequency scaling).
