# 🎧 Acoustic-Localization-Agent & Hardware Copilot

An automated workflow driven by local LLM Agents (currently integrating API for inference) designed for sound source localization simulation and hardware condition monitoring development.

## 📌 Project Overview
This project tackles the tedious and error-prone processes in hardware engineering and acoustic signal processing. By deploying a local AI Agent, we automate the pipeline from raw acoustic data processing (MATLAB) to dynamic hardware documentation generation.

### 🚀 Core Automated Workflows

#### 1. MATLAB Simulation Automation
* **Data Parsing:** The agent automatically reads large `.txt` dataset files collected from a tetrahedral MEMS microphone matrix.
* **Algorithm Execution:** Automatically triggers MATLAB scripts to run **TDOA (Time Difference of Arrival)** for coarse range estimation, followed by **OMP (Orthogonal Matching Pursuit)** for precise 3D spatial intersection.
* **Signal Purification:** Executes bandpass filtering and time-domain windowing to counter high background noise in semi-anechoic environments.

#### 2. Hardware Engineering Sync
* **BOM Management:** Reads local project files and dynamically updates the Bill of Materials (`.csv`), ensuring accurate pricing and model tracking for critical components like the **STTS751 Temperature Sensor**.
* **Documentation:** Automatically updates the product manual for the analog ultrasonic microphone amplifier circuit, specifically tracking GPIO pin assignments (e.g., QSPI and SPI1) for the **STM32L4R9VIT6** MCU.

## 🛠️ Tech Stack & Hardware Setup
* **Agent Framework:** Local Terminal Agent Workflow
* **Algorithms:** MATLAB, OMP, TDOA, GCC-PHAT
* **Microcontroller:** STM32L4R9VIT6
* **Sensors:** * STTS751 (Temperature Sensor)
  * ICS-43434 (Analog Microphone)
  * IM68A130V01 (Digital Microphone)

## 🔜 Next Steps / API Integration
Currently migrating the core reasoning engine to handle larger context windows for automated IEEE paper analysis (Compressed Sensing & OMP improvements) and higher throughput for massive `.txt` data processing.
