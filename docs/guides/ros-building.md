# ROS building
ROS uses CMakeLists.txt file to build packages.

this guide does not pretend to explain all of the options these file provides,
but some simple examples that help the user build their first packages with catkin.

## The build Flow 
first catkin reads the CMakeLists.txt inside your worspace 



## common pitfalls 

CMake Error at /opt/ros/noetic/share/catkin/cmake/empy.cmake:30 (message):
  Unable to find either executable 'empy' or Python module 'em'...  try
  installing the package 'python3-empy'

```bash
catkin build -DPYTHON_EXECUTABLE=/usr/bin/python3 -DPYTHON_INCLUDE_DIR=/usr/include/python3.7m
```