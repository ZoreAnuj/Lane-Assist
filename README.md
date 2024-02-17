# Lane-Keeping-Assist-on-CARLA
## Introduction

![carla](https://github.com/ZoreAnuj/Lane-Assist/assets/95142805/5dad8e28-f5ed-4d09-873e-1a2f4d887fa2)

Reference: [Introduction to Self-Driving Cars](https://www.coursera.org/learn/intro-self-driving-cars) course of [Self-Driving Cars Specialization](https://www.coursera.org/specializations/self-driving-cars?) on Coursera.org.

Lane Keeping Assist function by applying pure pursuit and Stanley methods for lateral control and PID controller for longitudinal control using Python as the programming language.

The waypoints and corresponding velocities for the track are pre-defined.

## Prerequisites

CARLA loader requires **Ubuntu 16.04 or later** to run

## How to run it
First clone this repository and put it under **PythonClient** directory.

### 1. Load the simulator
Open a terminal and do `cd ~/opt/CarlaSimulator`.

Then do `./CarlaUE4.sh /Game/Maps/RaceTrack -windowed -carla-server -benchmark -quality-level=Low -fps=30
`
### 2. Run the LKA controller

Open another terminal and do `cd ~/opt/CarlaSimulator/PythonClient/Lane-Keeping-Assist-on-CARLA`.

(optional) do `sudo apt-get install python3-tk` in case you do not have `Tkinter` module.

Run `python3 module_7.py` to execute the controller(default is MPC control method)


### 3 control methods:

MPC - `python3 module_7.py --control-method MPC`

Stanley - `python3 module_7.py --control-method Stanley`

Pure Pursuit - `python3 module_7.py --control-method PurePursuit`

The vehicle should starting driving and following the track.

## Simulation results
The images shown below is the result of vehicle trajectory(MPC, Stanley and Pure Pursuit method).

The green line is the track(ground truth) and the orange line is the trajectory.

![trajectory_MPC](https://github.com/ZoreAnuj/Lane-Assist/assets/95142805/d9cd1a8b-0e11-43f3-be39-1a8c247c05cd)

![trajectory_PurePursuit](https://github.com/ZoreAnuj/Lane-Assist/assets/95142805/1a25ba64-4e7f-4f07-a3fa-0fc8ec16b109)

![trajectory_Stanley](https://github.com/ZoreAnuj/Lane-Assist/assets/95142805/51b99dd8-9f35-4f02-81a7-a1369225c47d)
