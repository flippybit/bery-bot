## Retrieving a Cloud point from the camera node
Prerequisites
* intel realsense camera
* simple_cloud_node code (TODO link to github with the workspace/or node)
1.  Install ROS intel realsense camera 
    1. realsense2_camera is available as a debian package of ROS distribution. It can be installed by typing:
        ```bash 
        sudo apt-get install ros-$ROS_DISTRO-realsense2-camera
        ```
2.  Run realsense camera node.
    ```bash
    roslaunch realsense2_camera rs_camera.launch
    ```
3.  Open rviz to view the camera published topics
    ``` bash
    rviz
    ```
4.  Subscribe to the published topics.
    1.  run our custom node that subcribes to the point cloud topic.
    2.  recive pointclouds frames.
    3.  process the frame.
    4.  output a message.

### our main goal in this spike is to gain an understanding into how to complete the perception pipeline the main goal is to be capable of settinga traking marker on the object recognized by our image recognition algorithm.
