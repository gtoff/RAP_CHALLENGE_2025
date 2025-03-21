# RAP_CHALLENGE_2025
Graded RAP Assignment for FS2025 to be demoed in presence (showing live simulation or video) during the last lecture of the course and to be turned in by the end of the last lab session.

## Setting
You are tasked with writing the software for a helpful mobile manipulator to be used in simple household tasks (e.g., finding, picking, and placing objects).

You have to leverage the power of an LLM with function calling (i.e., "tools") to provide a simple human-robot interface (HRI) for non-technical users to control the robot.
An initial simple example is provided here: https://github.zhaw.ch/RAP-EN/rosa_summit

Inspirational examples of what can be achieved (and which "tools" are used) are for instance BUMBLE (https://robin-lab.cs.utexas.edu/BUMBLE/) or Tidybot (https://tidybot.cs.princeton.edu/)

## Goals

The minimal requested robot functionality (grade=4) should be as follows:

* In a first "installation session" the user guides the robot to use a depth camera to build both a 3D and a 2D map of the household environment. At the end of the session the maps should be saved for further use (e.g., navigation);
* The robot should be able to navigate using the map to reach specific landmarks (e.g., the kitchen, the living room) as per user request;

A grade of 5 will be assigned on correct implementation of the following functionality:

* The robot should be able to find an object (e.g., through an Apriltag marker), pick it, and bring it to another room upon user request.

Any extra functionality / more general approach (e.g., using perception / object detection rather than a marker) for the provided tasks will be graded on top.

## Conditions, Hints, Assumptions

Hints and simplifying assumptions:
* Use ROS2 Jazzy and the icclab_summit_xl robot simulated in Gazebo;
* You are allowed to use anything you find online, including AI for code generation. You should however be able to explain the code and the functioning of your project upon review;
* You have **complete freedom** in the implementation, including adding **extra functionality** / complexity (e.g., using TTS to interact with the robot, using a different technology to interact with the LLM [e.g., https://github.com/RobotecAI/rai/ ], using semantic segmentation / object detection rather than markers) or a different robot. Extra functionality gives more points. Ask your teacher if you need help (e.g., setting up a specific Web UI for robot interaction);
* You can use any Gazebo model / starting world file you find online to create your household world or design your own. Keep it bounded (e.g., with a wall) and small for simulation and demo (e.g., 40 sqm). To simplify things don't place doors between rooms;
* Don't worry about simulation glitches (e.g., the simulated gripper doesn't hold a grasped object), I will grade your code (i.e., what it would be able to do) and not the simulator;
* Some other references of (possibly) useful projects are: Nav2, rtabmap, yolov8_ros;


## Deliverables (for grading)

**Note**: Your code should strive to use other ROS2 packages without requiring their modification. You may however copy or include the scripts and launchfiles from other projects if needed. You are expected to use package dependency configuration or an install script to include ALL dependency installation for your project.

Required deliverables (in a single git repository, one or more ROS packages at your choice):
* A .world file modeling your household environment to be used in Gazebo;
* The launchfile(s) to start the simulation and the robot interaction;
* Any other required source code to implement the requested functionality;
* A README.md describing the repository, its installation and usage

During the final lecture you are expected to give a 15 min presentation and demo (part of the grading) including:
* what goals you managed to complete
* for each goal what were your main difficulties, which alternatives you tried, and how you finally decided to implement it
* a live or recorded demo

## Further hints

* ROS2 launchfiles can be complicated. We suggest you copy into your package the launchfiles you have used during the labs for doing similar things.

