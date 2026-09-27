You can see the all results in the world file of this project
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Conformal (Cylindrical) Telemetry Antenna for High-Speed ​​Munitions
Design and Analysis of a Beam-Steering Microstrip Patch Antenna Array for 5G and 6G Systems

Project Objective
The primary objective of this project is to design and analyze—within an electromagnetic simulation environment—Beam Steering technology, which is utilized to enhance capacity and signal quality in 5G and beyond high-speed communication systems. While conventional antennas radiate energy equally in all directions or in a fixed direction, modern communication systems require energy to be focused solely on the intended user. This project aims to steer the main beam electronically to a desired angle by adjusting the timing of electrical signals fed to an array of side-by-side microstrip patch antennas, without employing any mechanical moving parts.
The study began with the design of a single patch antenna operating at a resonant frequency of 2.25 GHz; it was subsequently expanded to 1x2 and ultimately 1x4 phased-array antenna configurations to maximize directivity and beam-steering capability.
Phase: Single Microstrip Patch Antenna Design
In the initial phase of the project, a single microstrip patch antenna—the fundamental building block of the antenna array—was designed.
Geometry and Feeding: A structure featuring a fully copper-clad bottom layer on an FR4 substrate was utilized. The antenna is fed via a vertical pin extending from the bottom layer to the center of the patch.
Impedance Matching and Error Mitigation: An insulating gap was created in the ground layer to prevent the signal pin from short-circuiting to the ground. Additionally, to enable the antenna to radiate into free space, the simulation boundary conditions were set to "Open (add space)," and a Discrete Port was connected between the appropriate terminals (the pin and the ground). Results: As a result of the dimensional optimization, the antenna resonated at exactly 2.25 GHz. The S11 (return loss) dropped to the -13 dB level, achieving an impedance match of over 95%.

Radiation Performance: The directivity of the single antenna was measured at 7.65 dBi and the radiation efficiency at 79%, and it was observed that energy was successfully radiated along the Z-axis.


Stage 2: 1x2 Antenna Array Design
Following the successful operation of the single antenna, the system was upgraded to a 1x2 configuration to enable beam steering.
Array Configuration: To prevent electromagnetic coupling between the antennas, a spacing equal to half the free-space wavelength (66.6 mm) was set between their centers. The ground plane and substrate were extended along the X-axis to accommodate this spacing.
Isolation Analysis: When the two antennas operated side-by-side, the energy leakage between them (S2,1 parameter) remained at the -17.5 dB level, demonstrating effective isolation between the antennas.
Beam Steering Test: A phase of 0 degrees was applied to Port 1, and 90 degrees to Port 2. This phase difference deflected the physical beam exactly 19 degrees to the right of the Z-axis. Directivity increased from 7.65 dBi to 9.76 dBi, and the beamwidth was measured at 45.3 degrees.




Stage 3: 1x4 Phased Array Antenna and Advanced Beam Steering
In the final stage of the project, the number of antennas was increased to four to transform the beam into a much narrower, more precise, and longer-range "laser-like" beam.
Frequency Optimization: As the number of antennas increased, the resonant frequency shifted to 2.09 GHz due to mutual coupling. To compensate for this physical effect, the patch length (L parameter) was reduced to 40 mm, precisely locking the system back to a center frequency of 2.25 GHz. The S-parameters for all four antennas were found to be flawless and matched.
Steering to the Right: Phase shifts of 0°, 90°, 180°, and 270° were applied to the ports, respectively.
•	Gain increased significantly, reaching a level of 12.2 dBi.
•	Beamwidth decreased from 45 degrees to 26.5 degrees, maximizing focus.
•	The main beam was steered exactly 27.0 degrees to the right.

Left-Hand Steering: Phase shifts of (0, -90, -180, -270) degrees are applied to the ports, respectively.
•	Gain: 12.2 dBi
•	26.5 degrees
•	-27.0 degrees leftward rotation

Conclusion and Evaluation
Within the scope of this project, electromagnetic theory and antenna array principles were successfully implemented using the CST Studio environment. Through an iterative design process, challenging RF (Radio Frequency) issues—such as frequency matching, port isolation, and inter-antenna coupling—were resolved.
The resulting 1x4 phased array antenna model features high gain (12.2 dBi), a narrow beamwidth (26.5 degrees), and the capability to scan to desired angles using electronic signals without the need for mechanical components. These characteristics make the design a viable, professional-grade model for modern 5G and 6G communication systems and radar equipment. Analysis of the system's S-parameters confirmed consistent results, demonstrating excellent overall performance.
