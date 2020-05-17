## robot_math_tools
This package includes my favorite libraries and classes of math and geometry operations for robots.

Includes stripped-down versions of:
- [pyquaternion](http://kieranwynn.github.io/pyquaternion/): An amazing full-featured Python module for representing and using quaternions. 
- [modern_robotics](https://github.com/NxRLab/ModernRobotics): The Python module from the code in "Modern Robotics: Mechanics, Planning, and Control Code Library" which contains the code library accompanying [Modern Robotics: Mechanics, Planning, and Control](http://hades.mech.northwestern.edu/index.php/Modern_Robotics) (Kevin Lynch and Frank Park, Cambridge University Press 2017).
- [mathlib](https://github.com/NxRLab/ModernRobotics): A c++ [Mathlib](https://github.com/nbfigueroa/mathlib) math library developed at LASA library at EPFL.


---
## System Requirements
* ROS Indigo in Ubuntu 14.04.
* ROS Kinetic in Ubuntu 16.04
* Other distros not tested.

## Installation, Dependencies and Compilation
Do the following steps:
* In your catkin src directory clone the repository
```
$ git clone https://github.com/nbfigueroa/robot_math_tools.git
```
* wstool gets all other git repository dependencies, after the following steps you should see extra catkin 
  packages in your src directory.
```
$  wstool init
$  wstool merge robot_math_tools/dependencies.rosinstall 
$  wstool up 
```
* Query and installs all libraries and packages 
```
$ rosdep install --from-paths . --ignore-src --rosdistro indigo 
```
* Finally complie
```bash
  $ cd ~/catkin_ws
  $ catkin_make
  $ source devel/setup.bash
  $ catkin_make
```
  You might need to source the `./bashrc` file and compile again if the first compliation could not find some of the in-house dependencies. If `roscd` doesn't find the compiled packages run `rospack profile`.


---
## Contact
Maintainer: [Nadia Figueroa ](https://nbfigueroa.github.io/)(nadiafig @ mit dot edu)

<!-- ## License
- This code is released under MIT license. -->
