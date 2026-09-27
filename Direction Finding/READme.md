You can see the schematic of the results in the word file.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Direction Finding and Interferometer Antenna Array

1. Introduction and Project Objective
This report covers the design, optimization, and electromagnetic simulation processes of an Ultra-Wideband (UWB) Antipodal Vivaldi Antenna model, developed as part of an individual R&D project focused on high-frequency RF and microwave systems. In direction-finding and signal-tracking applications requiring wide-spectrum scanning, maintaining control over the antenna's impedance bandwidth, radiation directivity, and cross-polarization levels is of critical importance. To meet these engineering requirements, the Antipodal Vivaldi architecture—which ensures high-frequency stability—was selected for the design, and its analysis was conducted using the CST Studio environment.
2. Material Selection and Geometric Parameters
A low-loss Rogers series laminate was selected as the substrate material to minimize dielectric losses (tan δ) and preserve signal integrity in high-frequency (X-Band and above) applications. The physical length and aperture width were optimized to bring the antenna's cutoff frequency to the target levels and to suppress reflections occurring at the transition to free space.
Design Parameters:
Dielectric Material: Rogers (Low-loss high-frequency laminate)
Substrate Thickness (h): 0.508 mm
Conductor Thickness (M_t): 0.035 mm (Copper)
Total Length (L): 65 mm
Aperture Width (W): 60 mm

3. Parametric Optimization Process
A parametric sweep was conducted on the microstrip feed width (W_feed) and the curvature ratio (R) of the arms expanding into space to ensure a 50-ohm characteristic impedance match and to eliminate ripples within the operating band. It was observed that impedance matching improved as the W_feed parameter was narrowed, while the R parameter directly influenced the impedance taper at the radiating aperture. As a result of the optimizations, the ideal feed width was set to W_feed = 0.8 mm and the curvature ratio to R = 0.2.

4. Electromagnetic Simulation Results (S11)
In the final simulation of the antenna—with its dimensions and curvature profile optimized—performed using the Time Domain Solver, the targeted UWB characteristic was successfully achieved. Increasing the physical length to 65 mm and the width to 60 mm extended the antenna's lower frequency limit down to the 2.2 GHz range and eliminated electromagnetic reflections at the aperture.

As shown in the graph, the antenna exhibits high impedance matching, ranging from -10 dB to -18 dB, across a wide operating band of 3 GHz to 18 GHz. In particular, the resonance point of -18 dB at approximately 11 GHz demonstrates the successful achievement of wideband energy transfer.

5. Radiation Characteristics and Directivity (Far-field Analysis)
To analyze the system's spatial radiation performance and directivity, 3D far-field monitor results were examined at frequencies of 6 GHz and 10 GHz.

6 GHz Performance: The antenna exhibits a highly uniform end-fire radiation pattern focused along the target main axis. A directivity gain of 5.54 dBi was achieved, and thanks to the low dielectric loss advantage of the Rogers material, the radiation efficiency stands at a near-perfect level of -0.17 dB. 
10 GHz Performance: As the frequency increased, the gain rose to 6.42 dBi, and the ability to focus on the target improved, thereby meeting X-band requirements.

6. Conclusion and Evaluation
The Antipodal Vivaldi antenna developed within the scope of this independent design project delivered continuous UWB performance across the 3–18 GHz range, thanks to its optimized dimensions, exponential curve profile, and low-loss Rogers substrate. The stability of the S11 parameters and the uniform end-fire gain observed in the 3D radiation patterns confirm that this concept is capable of high-performance operation in advanced microwave systems, such as wideband direction finding and RF spectrum analysis.
