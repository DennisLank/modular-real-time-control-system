# Modular Control Interface for the Quanser QArm

## Overview

This repository contains the full project code for a bachelor thesis focused on developing a modular and user-friendly control interface for the Quanser QArm.

The application was built with Dash (Python) and combines robot control, live camera streaming, object detection, dataset generation and voice interaction within a single local web interface.

The project is centered on practical system integration: connecting hardware control, computer vision, local data handling and interactive UI components in one coherent application.

---

## Main Features

- **Dashboard**
  - Central landing page for navigating the application and accessing its main functions.

- **Manual Control**
  - Direct control of the Quanser QArm via joint-based movement, Cartesian coordinate input and LED color control.

- **Live Feed**
  - Real-time camera streaming with support for both RGB and depth views.
  - Separate windows can be opened for the live image streams.

- **Scan Workflow**
  - Automated object scanning using a YOLO-based detection pipeline.
  - Detected objects are visualized in a table and a bird’s-eye view map.
  - Includes Pick & Place actions between detected objects or to manually specified coordinates.

- **YOLO Model Management**
  - Upload and selection of local `.pt` YOLO models.
  - Step-by-step dataset generation workflow with macro and micro image capture.
  - ZIP export of generated image datasets and optional e-mail delivery.

- **Voice Interaction**
  - Speech-to-text and text-to-speech support for selected robot and UI commands.

---

## Technical Structure

The application is organized into modular components, including:

- Dash-based frontend with tab-specific modules
- Robot control layer for the Quanser QArm
- Intel RealSense camera integration
- YOLO-based object detection
- MySQL-based storage for scan results
- Local Flask routes for RGB and depth MJPEG streams
- Speech input/output helpers for voice-driven commands

This modular structure was chosen to keep the system maintainable and to separate UI, hardware access, vision logic and data handling as clearly as possible.

---

## Technology Stack

- Python
- Dash
- Flask
- OpenCV
- Intel RealSense (`pyrealsense2`)
- Ultralytics YOLO
- MySQL
- SpeechRecognition
- pyttsx3
- NumPy / Pandas / scikit-learn

---

## System Requirements

- Windows 10
- Working internet connection (required for initial setup and speech recognition)
- Installed software:
  - Git
  - Anaconda or Miniconda
  - Local MySQL server
  - QUARC Control Suite (required for Quanser hardware access)

---

## Running the Application

The project is designed as a local Windows application.

The main application entry point is:

`dash_app.py`

The repository also includes Windows launcher files for starting the project environment.

Once started successfully, the interface runs locally at:

`http://localhost:8050`

---

## Project Background

This system was developed as part of a bachelor thesis in engineering.

The goal was to create a practical and modular control platform that combines robotic interaction, computer vision and intuitive user access in a single application.

In addition to the control interface itself, the project also includes a workflow for collecting custom image data and integrating trained YOLO models back into the application.

---

## Scope and Limitations

This project is a prototype intended for research and demonstration purposes.

It was developed for a specific hardware setup consisting of the Quanser QArm and an Intel RealSense camera.  
As a result, parts of the implementation are hardware-dependent and tailored to this environment.

The application is not intended as a production-ready system, but as a modular experimental platform that can be extended and refined further.

---

## Contact

Dennis Marvin Lank  
Email: dennismarvinlank@gmail.com
