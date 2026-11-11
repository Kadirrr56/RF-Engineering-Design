# VLF (20 kHz) Magnetic Loop Antenna Design and CST Microwave Studio Simulation Report

### 1. Introduction and Project Objective
Systems operating in the Very Low Frequency (VLF) band—specifically around 20 kHz, such as those used for submarine communications, time/frequency broadcasts, and time-signal receivers—cannot be practically implemented using conventional dipole or monopole antennas, as their wavelengths are on the order of kilometers [cite: 9]. To overcome this physical constraint, magnetic loop antennas are preferred [cite: 9]. The objective of this study is to develop a 3D model of a single-turn magnetic loop antenna—resonant at 20 kHz—within the CST Microwave Studio environment, perform electromagnetic simulations, analyze its resonance and impedance characteristics, and demonstrate the process of matching it to a 50-Ohm system impedance using technical data [cite: 9].

![General Drawing](images/sekil1_genel_cizim.png)
*Figure 1: General Drawing [cite: 9]*

### 2. Design Parameters and Theoretical Background
Given the "electrically small" nature of a loop antenna operating in the VLF band, it is essential to compensate for its inductive reactance to achieve resonance at the target frequency [cite: 9].

* **Target Resonant Frequency (f0):** 20.00 kHz [cite: 9]
* **Tuning Capacitor (C):** A lumped capacitor with a value of 295 µF has been incorporated into the circuit to compensate for the antenna's inductance [cite: 9]. * **Feeding Method:** A discrete port excitation was applied directly via an opening at the top [cite: 9].
* **Mesh Strategy:** To avoid exceeding the 20,000-cell limit of the student version and to ensure solver stability, adaptive mesh refinement was optimized; the simulation was completed using a coarse yet stable tetrahedral mesh structure [cite: 9].

### 3. Simulation and Analysis Results

#### 3.1. Z-Parameters and Resonance Analysis (Z1,1)
The analysis of Z-parameters—the most fundamental indicator of antenna performance—clearly reveals the system's resonance state and ohmic losses [cite: 9]:

* **Imaginary Part:** Examination of the Z1,1 reactance plot shows that the curve crosses the 0 Ohm line (at 0.00068 Ω) at a frequency of 19.998 kHz [cite: 9]. This confirms that the 295 µF capacitor perfectly cancels out the antenna's inductance, placing the system in a state of pure resonance [cite: 9].

![Z-Parameters Imaginary Part](images/z_param_imag.png)
*Z1,1 Imaginary Part Plot*

* **Real Part (Ohmic Resistance):** At the resonance frequency, the total ohmic loss (conductor resistance) of the antenna was measured at 0.00123 Ω (1.23 mΩ) [cite: 9]. This extremely low resistance value aligns perfectly with the characteristic properties of VLF loop antennas[cite: 9].

![Real Part of Z-Parameters](images/z_param_real.png)
*Plot of the Real Part of Z1,1*

#### 3.2. Impedance Matching and S-Parameters (S11)
The significant discrepancy between the antenna's inherent ohmic resistance (1.23 mΩ) and the system impedance of standard RF equipment (50 Ω) was resolved through direct 3D port impedance optimization[cite: 9]. When the port impedance is matched to the physical resistance of the antenna[cite: 9]:
* A deep and sharp resonance dip at the -35 dB level is observed in the S11 (Return Loss) plot[cite: 9].
* This value indicates that a very high proportion of the power supplied from the port is transferred to the antenna at approximately 20.45 kHz, and that the resonance characteristics of the system are stable.

#### 3.3. Far-Field (Radiation and Efficiency) Analysis
The data obtained from the far-field monitor analysis conducted at a frequency of 20.45 kHz are as follows[cite: 9]:
* **Radiation Efficiency:** -58.70 dB (≈1.3×10^-4)
* **Directivity:** -63.10 dBi

**Engineering Commentary:** Due to their nature, electrically small loop antennas in the VLF band exhibit low radiation efficiency; the majority of the energy is dissipated as losses within the copper conductor[cite: 9]. This physical reality ensures that, while such antennas are inefficient as transmitters, they serve as excellent receivers due to the characteristics of ambient external noise [cite: 9]. The resulting 3D toroidal (donut-shaped) radiation pattern confirms the theoretical magnetic dipole radiation model.

![Far-field Analysis](images/farfield_analizi.png)
*3D Far-field Radiation Pattern*

### 4. Conclusion and Final Project Evaluation
In this study, rigorous mathematical calculations were successfully integrated with simulation tools from CST Microwave Studio. Software-related constraints—specifically mesh cell boundaries and port impedance mismatches—were resolved through analytical approaches. Furthermore, the project successfully completed all key stages, including achieving resonance in the VLF band, conducting Z-parameter analysis, optimizing impedance, and characterizing the far-field radiation.
