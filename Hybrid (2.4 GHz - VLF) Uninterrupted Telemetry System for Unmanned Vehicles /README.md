# VLF (20 kHz) Magnetic Loop Antenna Design and CST Microwave Studio Simulation Report

### 1. Introduction and Project Objective
In the Very Low Frequency (VLF) band—specifically for systems operating at 20 kHz (such as submarine communications, time/frequency broadcasts, and time-signal receivers)—traditional dipole or monopole antennas are impractical to implement because their wavelengths are on the order of kilometers [source: 9]. To overcome this physical limitation, magnetic loop antennas are preferred [source: 9]. The objective of this project is to design a single-turn magnetic loop antenna that resonates at 20 kHz using CST Microwave Studio, conduct environmental simulations, analyze its resonance and impedance characteristics, and provide the technical data required for impedance matching to a 50-ohm system [source: 9].

![General Drawing](images/sekil1_genel_cizim.png)
*Figure 1: General Drawing [source: 9]*

### 2. Design Parameters and Theoretical Background
Designing a loop antenna for the VLF band requires accounting for its "electrically small" structure, the associated inductive reactance, and the necessity of achieving resonance at the target frequency [source: 9]. * **Target Resonant Frequency (f0):** 20.00 kHz [source: 9]
* **Tuning Capacitor (C):** A lumped capacitor with a value of 295 µF has been added to the circuit to tune out the antenna's inductance [cite: 9].
* **Excitation Method:** Direct excitation via a discrete port is applied at the top-loading disk [cite: 9].
* **Mesh Strategy:** To remain within the 20,000-cell limit while ensuring solution stability, the simulation was performed using an adaptive mesh refinement approach, starting with a coarse yet stable tetrahedral mesh structure [source: 9].

### 3. Simulation and Analysis Results

#### 3.1. Z-Parameters and Resonance Analysis (Z1,1)
The analysis of Z-parameters—a fundamental indicator of antenna performance—clearly reveals the system's resonances and ohmic losses [cite: 9]:

* **Imaginary Part:** The Z1,1 reactance plot shows the curve crossing the 0-ohm line (at 0.00068 Ω) at a frequency of 19.998 kHz [cite: 9]. This confirms that the 295 µF capacitor perfectly cancels out the antenna's inductance, indicating that the system is at exact resonance [cite: 9]. ![Imaginary Part of Z-Parameters](images/z_param_imag.png)
*Graph of the Imaginary Part of Z1,1*

* **Resistive Component (Real Part / Ohmic Resistance):** At the resonance point, the total ohmic loss (conductor resistance) of the antenna was measured as 0.00123 Ω (1.23 mΩ)[cite: 9]. This extremely low resistance value is entirely consistent with the characteristics of VLF loop antennas[cite: 9].

![Real Part of Z-Parameters](images/z_param_real.png)
*Graph of the Real Part of Z1,1*

#### 3.2. Impedance Matching and S-Parameters (S11)
Given the significant disparity between the antenna's intrinsic ohmic resistance (1.23 mΩ) and the 50 Ω system impedance standard for RF equipment, the 3D port impedances were specifically solved[cite: 9]. When the port impedance is matched to the physical resistance of the antenna[cite: 9]:
* A deep, sharp resonance dip at the -35 dB level is observed in the S11 (Return Loss) plot[cite: 9].
* This indicates that, at approximately 20.45 kHz, a very high proportion of the power supplied to the port is transferred to the antenna, confirming the stability of the system's resonance characteristics[cite: 9].

![S11 Plot](images/sekil2_s11_grafigi.png)
*Figure 2: S1,1 Plot[cite: 9]*

#### 3.3. Far-field (Radiation and Efficiency) Analysis
The data obtained from the far-field monitor analysis, recorded at 20.45 kHz, are as follows[cite: 9]:
* **Radiation Efficiency:** -58.70 dB (≈1.3×10⁻⁴)[cite: 9]
* **Directivity:** -63.10 dBi[cite: 9]

**Engineering Commentary:** For electrically small loop antennas operating in the VLF band, the majority of the energy is dissipated as losses within the copper conductor[cite: 9]. While this physical reality renders such antennas inefficient as transmitters, it also makes them excellent receivers, particularly given the characteristics of ambient external noise[cite: 9]. The resulting 3D toroidal (donut-shaped) radiation pattern confirms the theoretical characteristics of magnetic dipole radiation[cite: 9].

![Far-field Analysis](images/farfield_analizi.png)
*3D Far-field Radiation Pattern*

### 4. Conclusion and Final Project Assessment
This project successfully integrated rigorous computational programming with the simulation tools provided by CST Microwave Studio[cite: 9]. Software-related constraints—such as mesh cell boundaries and port impedance mismatches—were addressed through analytical solutions. Furthermore, the key stages of the project—achieving resonance in the VLF band, conducting Z-parameter analysis, configuring impedance, and characterizing the far-field—were completed in their entirety[cite: 9].
