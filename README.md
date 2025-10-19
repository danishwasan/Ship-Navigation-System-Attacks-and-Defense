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
@article{VASAN2026104706,
title = {Cyber-attacks: Securing ship navigation systems using multi-layer cross-validation defense},
journal = {Computers & Security},
volume = {160},
pages = {104706},
year = {2026},
issn = {0167-4048},
doi = {https://doi.org/10.1016/j.cose.2025.104706},
url = {https://www.sciencedirect.com/science/article/pii/S0167404825003955},
author = {Danish Vasan and Mohammad Hammoudeh and Adel F. Ahmed and Hamad Naeem},
keywords = {Ship navigation system attacks, GPS spoofing, INS data corruption, Sonar manipulation, Depth control interference, Autopilot control interference, Collision avoidance system tampering, Sensor fusion tampering, Cross validation defense mechanisms},
abstract = {The safety and reliability of ship navigation systems are critical for secure maritime operations. With growing reliance on digital tools, these systems face increasing vulnerability to cyber–physical threats such as GPS spoofing, sensor manipulation, and control logic interference. This research presents a comprehensive threat model across key navigation subsystems and proposes a multi-layer defense strategy based on cross-sensor validation. Rather than relying on hardware redundancy or statistical anomaly filters, our framework validates sensor data and control decisions through consistency checks across GPS, INS, sonar, and depth systems. Standard filtering techniques, such as Kalman filters, are used for state estimation. Experimental simulations across various attack scenarios show that the proposed defense restores navigational accuracy and operational safety, reducing error by over 99% in most subsystems. A public dataset and codebase are released to support future maritime cybersecurity research on GitHub11Dataset and code available at: https://github.com/danishwasan/Ship-Navigation-System-Attacks-and-Defense..}
}
Free Access Link
https://kwnsfk27.r.eu-west-1.awstrack.me/L0/https:%2F%2Fauthors.elsevier.com%2Ftracking%2Farticle%2Fdetails.do%3Faid=104706%26jid=COSE%26surname=Vasan/1/01020199d0963a8e-62776654-144f-4a67-9a8f-f79716dd53dc-000000/p_cF684PcLrl53ujZqNZkf8cXTo=447

License

This repository is open-source and available under the MIT License. Contributions to expand and improve the dataset, scenarios, or defense mechanisms are welcome.
