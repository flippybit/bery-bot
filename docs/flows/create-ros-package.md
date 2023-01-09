# Create a ROS package

the ros.org link to this tutorial is here http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28c%2B%2B%29

## packages need to be contained in a catkin_workspace

### Create a catkin_ws if you dont have one already

1. create a catkin_ws this directory is were all our nodes will live

Make a folder/directory
```bash
mkdir -p catkin_tutorials_ws/src
```
Init the workspace 
```bash
catkin init
```
Build the workspace
```bash
catkin build
```
Source the workspace
```bash
source devel/setup.bash
```

  ### Create a package
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