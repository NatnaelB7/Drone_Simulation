# Drone Simulation

Simulate a drone in a VR environment of Genova, Italy.

## Table of Contents

- [Introduction](#introduction)
- [Used Tools](#used-tools)
- [Installation](#installation)
- [Usage](#usage)

## Introduction

The purpose of this project is to simulate a drone in a VR environment, specifically the city of Genova, Italy.

## Used Tools

- **Colosseum**: An open-source simulator for robotic and autonomous systems, built on Unreal Engine. It supports newer versions of Unreal Engine and provides a high-quality simulation environment.
- **Python 3.12.1**: A high-level, object-oriented programming language used for various purposes, including drone control scripts.
- **Unreal Engine v. 5.2.1**: A tool from Epic Games for game development, simulations, video editing, and rendering animations. Necessary plugins include:
  - **Cesium for Unreal**: Provides high-accuracy 3D geospatial data using Google Maps API.
  - **TCP Sockets Plugin**: Enables network communication between client and server.
- **Visual Studio v.2022**: An IDE for developing applications on various platforms.
- **D-flight Website**: Provides information on aerial restrictions for drones.

## Installation

To integrate Colosseum (AirSim) with Unreal Engine 5, follow these steps:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/CodexLabsLLC/Colosseum.git
    ```

2. **Install Dependencies**: Ensure you have Unreal Engine 5 and Visual Studio installed.

3. **Open Unreal Engine Project**:
    - Navigate to the `Unreal/Environments` directory in the cloned Colosseum repository.
    - Open the `.uproject` file with Unreal Engine 5.

4. **Build the Project**:
    - In Unreal Engine, click `File -> Generate Visual Studio project files`.

5. **Configure AirSim Plugin**:
    - Copy the `AirSim` folder into the `Plugins` directory of your `UAV_UGV` project. Create the directory if it does not exist.
    - In Unreal Engine, navigate to `Edit -> Plugins` and enable the AirSim plugin.

6. **Configure Settings**:
    - Copy the `settings.json` file from the AirSim repository to the root directory of your `UAV_UGV` project (`Document -> AirSim -> settings.json`).

7. **Set Up Environment**:
    - Use Cesium to construct the Genova environment by adjusting longitude and latitude.
    - Ensure your environment has sufficient space and appropriate surfaces for the drone to fly.
    - Add a `PlayerStart` actor to your level to define the initial spawn location for the drone.

8. **Build and Run the Project**:
    - In Unreal Engine, go to `File -> Generate Visual Studio project files`.
    - Open the generated Visual Studio solution and build the project.
    - Return to Unreal Engine and click `Play` to start the simulation. The drone should spawn and be controllable within your custom environment.

## Usage

To control the drone, follow these steps:

1. Navigate to the Python scripts directory:
    ```bash
    cd Python Scripts
    ```

2. Run the drone control script:
    ```bash
    python .\Test_drone_control.py
    ```
