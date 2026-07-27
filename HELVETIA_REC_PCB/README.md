# Project HELVETIA
Project HELVETIA's mission was to successfully build, launch and safely recover our rocket at the Spaceport America Cup 2022 (SACUP). 
It was designed to reach an apogee of 30,000ft with a total impulse of 40,960Ns.

## Recovery System
To briefly contextualize, here is an overview of the recovery system section:
![image](https://github.com/Bingsu64/portfolio/blob/main/HELVETIA_REC_PCB/Images/REC_Render.png)


Due to the competition requirements, our team utilized a Commercial Off-The-Shelf (COTS) flight computer for primary sensor logging.
To bridge the actuation and power needs, I designed a dedicated auxiliary board with Altium Designer, responsible for:
 - Power Distribution and Switching: Safely arming the system and switching power rails for deployment mechanisms
 - PWM Generation: Creating precise pulse-width modulation signals for servo motor control without requiring an onboard microcontroller (due to chip shortage)
 - Mission Reliability: Total Redundancy between the COTS and Student Researched and Developed (SRAD) flight computer to ensure reliable and safe recovery operations

Note on Avionics Architecture: While SACUP regulations mandated the use of a standard COTS flight computer (TeleMega) for official mission data logging, 
our project leadership also instituted an internal requirement to test a newly student-researched and developed (SRAD) flight computer. 
Project HELVETIA successfully served as the foundational flight-test vehicle, providing the critical empirical telemetry needed to prove the reliability 
of that SRAD flight computer to regulatory officials. Within this architecture, my direct ownership and design scope focused entirely on the auxiliary power-switching, 
PWM generation, and robust actuation hardware required for safe recovery execution.

## System Integration & Flight Validation
This auxiliary hardware was integrated directly into the rocket's recovery loop as a mission critical interface to manage physical deployment for both drogue and main parachute.
 - Beyond standard telemetry verification, our primary design and operational goal for the recovery team was simple: make a recovery system that just works
 - As the first team in ARIS history to successfully and safely land and recover our rocket, every testing procedure, safety checklist, and power-switching constraint was engineered around eliminating single-point failures
 - Flight data and test logs confirmed that the auxiliary power and actuation hardware executed deployment flawlessly under real flight conditions, securing 2nd place in the 30k ft category at SACUP 2022


## Key Takeaways & Engineering Lessons
 - Harsh Environment Design: Learned firsthand how physical vibrations and high-g forces dictate component selection, trace sizing, and layout constraints
 - System Simplicity: Saw the direct impact on system robustness by making a design simple
 - End-to-End Ownership: Managed the full lifecycle of a mission-critical PCB from initial schematic capture and layout to manufacturing, assembly, and bench/field verification
