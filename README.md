# RoboND-BuildMyWorld

The "Build My Robot project" is the first project that comes in Gazebo World lesson in Robotics Software Engineer Nanodegree Program. The purpose is to learn how to build a world with custom designed models and pre installed models in Gazebo. This project also has a plugin that welcomes at the begining of the simulation execution.

### Directory Structure
```
    .myrobot                           # 
    ├── images                         # Code output image                   
    │   ├── result.png
    ├── model                          # Model files of the two-wheeled robot
    │   ├── Building
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── robot
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script      
    │   ├── hello.cpp
    ├── world                          # Gazebo main World empty scene
    │   ├── office.world
    ├── CMakeLists.txt                 # Link libraries 
    └──README.md                             
```

### Steps to launch the simulation

#### Step 1 Update and upgrade the Workspace image
```sh
$ sudo apt-get update
$ sudo apt-get upgrade -y
```

#### Step 2 Clone the lab folder in /home/workspace/
```sh
$ cd /home/gazebo_ws/
$ git clone https://github.com/2sbsbsb/RoboND-BuildMyWorld
```

#### Step 3 Compile the code
```sh
$ cd /home/gazebo_ws/RoboND-BuildMyWorld/
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

#### Step 4 Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/gazebo_ws/RoboND-BuildMyWorld/build
```

#### Step 5 Run the Gazebo World file  
```sh
$ cd /home/gazebo_ws/RoboND-BuildMyWorld
$ gazebo world/office.world
```

### Output
The hello world message and the two-wheeled robot inside a Gazebo World should both launch as follow: 
![alt text](images/result.png)
