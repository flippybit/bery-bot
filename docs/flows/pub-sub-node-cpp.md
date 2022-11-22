# The simple publisher / subscriber node in ROS

the ros.org link to this tutorial is here http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28c%2B%2B%29

## in this guide we are writing a pubisher and a subcriber node for ROS

1.  first we need to have created a catkin_ws this directory is were all our nodes will live

make a folder/directory
```bash
mkdir -p catkin_tutorials_ws/src
```
init the workspace 
```bash
catkin init
```
build the workspace
```bash
catkin build
```
source the workspace
```bash
source devel/setup.bash
```

  ### 2. Create a package
Inside of the workspace we will create a ROS package this is were our nodes will live

```bash
catkin_create_pkg my_first_pkg std_msgs rospy roscpp
```
`catkin_create_pkg` --> what does this command do ?     
it does what is name suggests it builds a ROS package with some boiler plate.
```bash
├── CMakeLists.txt
├── include
│   └── my_first_pkg
├── package.xml
└── src

```