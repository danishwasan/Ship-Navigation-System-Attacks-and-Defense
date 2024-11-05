
# Dataset: Simulated Ship Navigation System Attacks

This dataset provides simulated data generated from a series of cyber-physical attack scenarios targeting critical subsystems of a ship’s navigation system. The dataset includes measurements and status indicators from various subsystems under normal and attack conditions, allowing researchers to study and develop defense mechanisms for maritime cybersecurity.

# Dataset Overview

This dataset comprises simulated scenarios covering multiple attack vectors, including GPS spoofing, INS (Inertial Navigation System) data corruption, sonar manipulation, depth control tampering, collision avoidance interference, autopilot manipulation, and sensor fusion disruption. Each scenario is designed to reflect realistic maritime cybersecurity threats. We provide CSV data for each subsystem’s behavior under both normal and attack conditions.

Data Collection Methodology

The dataset is generated using a custom Python simulation that mimics real-world navigation and attack conditions for critical subsystems, as detailed below:

	1.	Inertial Navigation System (INS): Records the ship’s position and velocity, with scenarios including INS data corruption attacks.
	2.	Sonar System: Logs detected underwater obstacles, with scenarios of false obstacle detection.
	3.	Depth Control System: Monitors the depth of the vessel with sensor tampering scenarios to induce incorrect depth readings.
	4.	GPS: Records the ship’s position from GPS readings, with scenarios simulating GPS spoofing.
	5.	Collision Avoidance System: Logs evasive actions taken by the system in response to detected obstacles, including false obstacles to test system interference.
	6.	Autopilot System: Logs the course adjustments made by the autopilot, with scenarios simulating course manipulation.
	7.	Sensor Fusion: Fuses data from various subsystems to estimate the overall state, with scenarios simulating fusion disruptions.

Each scenario in the dataset includes:

	•	Time: Timestamp for each recorded data point.
	•	Position (X, Y): The position of the ship on a 2D plane.
	•	Velocity (X, Y): The velocity components in the X and Y directions.
	•	Sonar Detections: Number of obstacles detected by sonar.
	•	Depth: Current depth of the vessel as monitored by the Depth Control System.
	•	GPS Position (X, Y): GPS-reported position, potentially compromised by spoofing.
	•	Course: Current course maintained by the Autopilot System.
	•	Evasive Action: Indicates whether an evasive action was taken by the Collision Avoidance System.
	•	Fused Position (X, Y): Combined position estimates from sensor fusion.
	•	Scenario: The scenario type, indicating the specific attack applied or if it was a normal operation.

Attack Scenarios

The dataset includes the following scenarios:

Scenario	Attack Description
Normal	No attacks; all systems operate under normal conditions.
INS_Attack	Introduces noise and drift into the INS readings, leading to inaccurate position and velocity measurements.
Sonar_Attack	Simulates false sonar detections, adding phantom obstacles to disrupt course.
Depth_Attack	Tampered depth readings cause erroneous depth adjustments.
GPS_Attack	GPS spoofing manipulates the vessel’s perceived position.
Collision_Attack	False data in the collision avoidance system, leading to either unneeded evasive actions or suppressed obstacles.
Autopilot_Attack	Introduces random deviations in the course adjustments by the autopilot.
SensorFusion_Attack	Simulates simultaneous disruptions in multiple sensors, compromising the sensor fusion output.

File Structure

All scenarios are consolidated into a single CSV file:

	•	Filename: submarine_navigation_data.csv
	•	Format: CSV with each row representing a timestamped data point for a particular scenario.

Example Usage

To load and analyze the data in Python:

import pandas as pd

# Load the dataset
df = pd.read_csv('submarine_navigation_data.csv')

# Display the first few rows
print(df.head())

Dataset Summary Table

Column	Description
Time	Timestamp for each data point.
Position_X	X-coordinate of the ship’s position from the INS.
Position_Y	Y-coordinate of the ship’s position from the INS.
Velocity_X	X-component of the ship’s velocity from the INS.
Velocity_Y	Y-component of the ship’s velocity from the INS.
Sonar_Detections	Number of obstacles detected by the sonar system.
Depth	Current depth of the vessel, as managed by the Depth Control System.
GPS_Position_X	X-coordinate of the position reported by GPS.
GPS_Position_Y	Y-coordinate of the position reported by GPS.
Course	Current course setting by the Autopilot System.
Evasive_Action	Binary indicator (1 or 0) of whether an evasive action was taken by the Collision Avoidance System.
Fused_Position_X	X-coordinate of the fused position estimate from multiple subsystems.
Fused_Position_Y	Y-coordinate of the fused position estimate from multiple subsystems.
Scenario	Scenario type (e.g., Normal, INS_Attack, etc.), indicating attack or normal status.

Repository Structure

The repository contains the following:

	•	Code: Python scripts for generating the dataset.
	•	Dataset: CSV files for each attack scenario.
	•	Documentation: Detailed explanations of each subsystem, attack scenario, and defense mechanism.

This README provides researchers and practitioners with clear insights into the dataset’s structure, methodology, and potential applications, facilitating advancements in ship navigation system cybersecurity research.