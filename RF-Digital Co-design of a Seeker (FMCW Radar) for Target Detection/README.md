# Design and Simulation of a 4-Element Microstrip Array Antenna for a 24 GHz FMCW Radar Seeker Head

### 1. Project Abstract
In this project, a 4-element (2x2) microstrip patch array antenna—designed for the 24 GHz ISM band—was developed for FMCW (Frequency Modulated Continuous Wave) radar seeker head applications, which are typically employed in military/defense systems and automotive radar [cite: 8]. Electromagnetic simulations were conducted using CST Studio Suite, utilizing Rogers RO4350B as the substrate material; quarter-wave transformers and inset feed optimizations were implemented to minimize return loss [cite: 8]. The final design achieved a return loss (S11) of -15.5 dB at a resonant frequency of exactly 24.0 GHz, with a gain of approximately 6.9 dBi [cite: 8].

### 2. Design Parameters and Material Selection
For the antenna design, industry-standard laminate materials were selected, as they offer low dielectric loss and stable performance at high frequencies [cite: 8]. * **Substrate Material:** Rogers RO4350B[cite: 8]
* **Dielectric Constant (ϵr):** 3.16[cite: 8]
* **Substrate Thickness (h):** 0.254 mm[cite: 8]
* **Copper Conductor Thickness (Mt):** 0.035 mm (1 oz copper)[cite: 8]
* **Center Operating Frequency:** 24.0 GHz[cite: 8]

**Geometric Values ​​Obtained After Optimization:**
| Parameter | Value |
| :--- | :--- |
| **Physical Width of the Patch (W)** | 4.15 mm[cite: 8] |
| **Physical Length of the Patch (L)** | 3.41 mm[cite: 8] |
| **Feed Line Width (Wf)** | 0.55 mm (50 Ohm system impedance)[cite: 8] |
| **Quarter-Wave Transformer Width** | 1.03 mm (35.35 Ohm impedance bridge)[cite: 8] |
| **Inset Feed Depth (Fi)** | 1.0 mm[cite: 8] | ### 3. Engineering Process and Methodology
Impedance mismatches and frequency shifts encountered during the design phase were resolved through systematic engineering steps[cite: 8]:
* **Impedance Bridge and Feed Network:** Since the impedance drops when the branches are combined in a 2x2 array configuration, quarter-wavelength transformers with a calculated width (1.03 mm) were integrated before the T-junctions[cite: 8]. All copper structures were unified into a single component using the "Boolean Add" command[cite: 8].
* **Resonance and Frequency Tuning:** Through parametric sweeps and optimization of the patch length (L=3.41 mm), the antenna resonance was precisely locked to the target 24.0 GHz band[cite: 8].
* **Impedance Matching (S11):** Power transfer efficiency was maximized by adjusting the notches and transformers, bringing the return loss to -15.5 dB[cite: 8].

### 4. Simulation Results and Analysis

**S11 Return Loss:**
* **Resonance frequency:** 24.0 GHz[cite: 8]
* **S11 value:** -15.5 dB (indicating that more than 97% of the power is successfully radiated by the antenna)[cite: 8].

**Far-field Results:**
* Based on the 3D radiation analysis, the maximum gain (Directivity/Gain) was measured at 6.9 dBi[cite: 8]. * It has exhibited a high-directivity characteristic, focused on a single main lobe, in a manner that meets the requirements for a seeker head [cite: 8].

### 5. Conclusion and Applications
The 24 GHz microstrip array antenna structure developed in this project offers an industry-standard solution for FMCW radar seeker head systems, featuring low cost, a low profile, high gain (6.9 dBi), and excellent impedance matching (-15.5 dB) [cite: 8]. The system is well-suited for applications such as missile seeker heads, radars for defense-industry UAVs/UCAVs, and 24 GHz safety/radar sensors for the automotive sector [cite: 8].
