# KUKA Robot Application - Spot Welding & Handling

This repository contains a complete program and configuration backup for a KUKA industrial robot application, designed for a spot welding or material handling task. The project is built for the KUKA KRC4 controller architecture.

---

## Project Overview

This application demonstrates a structured approach to robot programming, separating the main logic, background tasks, and machine configuration. The core of the project is designed to run a specific sequence of operations using a spot welding gripper.

---

## Key Components

* **`cell.src`**: The main entry point for the entire robotic cell, responsible for initialization and calling sub-programs.
* **`honai.src` / `honai.dat`**: The primary motion and logic program, containing the robot's main operational sequence and path data.
* **`sps.sub` (Submit Interpreter)**: A background PLC-like task that manages I/O, safety signals, and overall cell state machine logic.
* **`KRC/STEU/Mada/`**: Contains the core machine data (`$machine.dat`) and configuration files, defining the robot model, tools, and system parameters.
* **`Gripper_SpotTech/`**: A technology package with dedicated programs for controlling a spot welding gripper, including weld schedules and tool-specific logic.

---

## Technical Details

* **Robot Controller**: KUKA KRC4
* **Programming Language**: KUKA Robot Language (KRL)
* **Core Concepts**:
    * Structured programming with sub-routines.
    * Use of a background task (`sps.sub`) for persistent logic.
    * Separation of code (`.src`) and data (`.dat`).
    * Configuration of tooling and I/O.

---

## How to Use

This project is a backup archive. To view or run it, you need KUKA's proprietary software:

1.  **KUKA WorkVisual**: Can be used to open, edit, and deploy the project to a controller.
2.  **KUKA.Sim Pro**: Can be used to create a digital twin of the robot cell and run the program in a 3D simulation environment.