# Ship-Navigation-System-Attacks-and-Defense

This repository provides a comprehensive dataset and simulation resources focused on cybersecurity for ship navigation systems. It includes datasets generated from various cyber-attack scenarios, targeting critical subsystems such as GPS, Inertial Navigation System (INS), sonar, autopilot, depth control, and sensor fusion. Additionally, this repository offers simulation scenarios and defense mechanism models designed to test and enhance the resilience of ship navigation systems against adversarial threats.

# What We Propose

Traditional defenses often rely on hardware redundancy, which can still be vulnerable to spoofed signals. Instead, this project introduces a software-only onboard defense mechanism that can be integrated into existing ship navigation systems:

	•	Cross-Sensor Consistency Checks: Compare independent sensors (GPS, INS, sonar, radar, depth) and flag anomalies when data does not match expected consistency.

	•	Sensor Fusion with Kalman Filtering: Integrate multiple sensor inputs to suppress noise and minimize the impact of compromised data.

	•	Control Validation Logic: Allow course corrections or evasive actions only when sensor data is consistent and trustworthy.

This multi-layer defense approach ensures that ships can detect, filter, and mitigate manipulated data in real time, without requiring new hardware.

Repository Structure

	•	data/: Contains the dataset generated from simulated cyber-attacks on ship navigation subsystems. Each file includes attack labels, timestamps, and associated data points for different attack scenarios.
	•	scenarios/: Provides configurations and descriptions for each attack scenario used to simulate cyber threats on navigation systems, detailing specific parameters and configurations.

Key Features

	•	Multi-Layer Cross-Validation Defense: Our approach demonstrates over 99% effectiveness in mitigating cyber-attacks on ship navigation systems. Scripts and scenarios provided in the repository demonstrate these defense mechanisms across various navigation subsystems.
	•	Scenario-Based Attack Models: Covering GPS spoofing, INS data corruption, sonar manipulation, and autopilot interference, these scenarios aim to replicate real-world navigation system vulnerabilities.
	•	Dataset for Public Use: This dataset is available for research purposes and aims to support the cybersecurity community in developing new defense strategies for maritime navigation systems.

How to Use

	1.	Clone the repository.
	2.	Refer to the README.md in each folder for detailed instructions on using the dataset and running the simulation scenarios.
	3.	Follow the scripts in the Scenarios/ directory to replicate the simulation and test the effectiveness of the multi-layer cross-validation defense mechanisms.

Citation

Will Be Availabe Soon (Cyber-Attacks: Securing Ship Navigation Systems using Multi-Layer Cross-Validation Defense)

License

This repository is open-source and available under the MIT License. Contributions to expand and improve the dataset, scenarios, or defense mechanisms are welcome.
