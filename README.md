# BA2 Project

This is the working directory for the BA2 project in computer science.
Before compiling this project, you first need to install

- ARGoS3 (version beta56) - https://github.com/ilpincy/argos3 (commit `623fb873eaaddb22747dceb13f917790bad33f5e`)
- argos3-epuck - https://github.com/demiurge-project/argos3-epuck
- argos3-arena - https://github.com/demiurge-project/argos3-arena
- ROS Melodic - http://wiki.ros.org/melodic/Installation/Ubuntu

## Compiling the project

In a terminal:

```bash
git clone https://github.com/Projet-BA2/Project-Workspace.git BA2_project_workspace
cd BA2_project_workspace
catkin_make
```

## Launching an experiment

1) Initialize ROS:

```bash
roscore
```

2) In a separate terminal

```bash
cd BA2_project_workspace
argos3 -c experiments/YOUR_EXPERIMENT.argos
```

## Creating new controllers/loop functions

1) Create a new folder for your new code in `BA2_project_workspace/src/BA2_project/controllers/` (or `BA2_project_workspace/src/BA2_project/loop_functions/`). You can copy the template directory and modify the C++ files and the `CMakeLists.txt` file inside to adapt them to your new code.

2) Add your new directory in the `CMakeLists.txt` file in `BA2_project_workspace/src/BA2_project/controllers/` (or `BA2_project_workspace/src/BA2_project/loop_functions/`).

3) Compile:

```bash
cd BA2_project_workspace
catkin_make 
```

## Creating new experiments

Simply create a new `.argos` file in the experiments directory. No need to compile.
