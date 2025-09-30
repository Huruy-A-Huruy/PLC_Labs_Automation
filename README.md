# PLC Automation Labs

This repository contains Programmable Logic Controller (PLC) labs completed as part of my Electrical Engineering Technician program.  
The labs were implemented using Rockwell Logix Designer and demonstrate ladder logic programming for automation tasks.

## 🛠️ Tools & Skills
- **Software:** Rockwell Logix Designer 5000
- **Concepts:** Ladder Logic, ONS (One-Shot), MOV, ADD, SUB, CPT, CMP, RTO, Timers
- **Applications:** Industrial automation, process control, event-driven logic.

## 📑 Files
- `lab4a.pdf` → Ladder logic report for Lab 4A.
- `lab4b.pdf` → Ladder logic report for Lab 4B.
- `lab4a_description.md` & `lab4b_description.md` → Detailed explanations of each lab.

# Lab 4A – Increment/Decrement Control

### Objective
To design a ladder logic program that allows the user to increment, decrement, and reset an output voltage using push buttons.

### Features
- **Increment Function:** Push button PB_0 increases voltage by 500 units.
- **Decrement Function:** Push button PB_1 decreases voltage by 500 units.
- **Reset Function:** Push button PB_2 resets the output to a default value (500).
- **ONS Instruction:** Ensures that each push button press is only counted once.

### Instructions Used
- **MOV** – Move default values.
- **ADD** – Increment values.
- **SUB** – Decrement values.
- **ONS (One-Shot)** – Prevents multiple triggers from one press.

### Applications
This lab demonstrates **basic user input control logic**, useful in:
- Machine parameter adjustment.
- Operator-controlled setpoints in automation systems.

# Lab 4B – Temperature Control & Timers

### Objective
To design a ladder logic program that monitors a temperature input and controls two lamps (High and Low) based on a setpoint and deadband values. The system also measures the ON time of the lamps using a retentive timer.

---

### Features
- **Deadband Control:**
  - Calculates upper and lower threshold values from the setpoint ± deadband.
  - Ensures stable switching of outputs to prevent rapid toggling.
  
- **Lamp Control:**
  - Turns ON **Lamp H** when the temperature is above the upper threshold.
  - Turns ON **Lamp L** when the temperature is below the lower threshold.
  - Both lamps turn OFF when the temperature is within the deadband range.
  
- **Timer Measurement:**
  - Uses an **RTO (Retentive Timer On)** to accumulate total ON time of the active lamp.
  - **RES instruction** allows resetting the accumulated time when needed.
  
- **User Input:**
  - Push button PB_1 resets the timer.
  - Temperature setpoint and deadband values can be adjusted by the operator.

---

### Instructions Used
- **CPT (Compute):** Calculates upper and lower thresholds.  
- **CMP (Compare):** Compares current temperature with thresholds.  
- **OTE (Output Energize):** Controls lamps based on compare results.  
- **RTO (Retentive Timer On):** Measures accumulated ON time.  
- **RES (Reset):** Resets timer values.  

---

### Applications
This lab demonstrates how to implement **process control with feedback** in ladder logic, applicable to:
- HVAC systems.  
- Industrial ovens or cooling systems.  
- Safety monitoring (temperature-sensitive operations).  

---

### Files
- **lab4b.pdf** – Full ladder logic implementation and screenshots.  

