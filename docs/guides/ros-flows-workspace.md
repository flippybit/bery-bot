# ROS - Flows
## workspace building flow

1. Build the workspace folder 
    ```bash
    mkdir -p catkin_examples_ws/src
    ```
2. Enter the newly made folder `catkin_examples_ws`  
    ```bash
    cd catkin_examples_ws
    ```
3. Initialize the workspace folder
    ```bash
    catkin init
    ```
    expected output:
    ```{toggle}
    ```{figure}..docs/imgs/real-berries.png
    ```

4.  Build the workspace folder with `catkin build`
    ```bash
    catkin build
    ```


a block toggle:
```{toggle}
```bash
fire@fire-box:~/catkin_example_ws$ catkin init
Initializing catkin workspace in `/home/fire/catkin_example_ws`.
-----------------------------------------------------------------
Profile:                     default
Extending:             [env] /opt/ros/noetic
Workspace:                   /home/fire/catkin_example_ws
-----------------------------------------------------------------
Build Space:       [missing] /home/fire/catkin_example_ws/build
Devel Space:       [missing] /home/fire/catkin_example_ws/devel
Install Space:      [unused] /home/fire/catkin_example_ws/install
Log Space:         [missing] /home/fire/catkin_example_ws/logs
Source Space:       [exists] /home/fire/catkin_example_ws/src
DESTDIR:            [unused] None
-----------------------------------------------------------------
Devel Space Layout:          linked
Install Space Layout:        None
-----------------------------------------------------------------
Additional CMake Args:       None
Additional Make Args:        None
Additional catkin Make Args: None
Internal Make Job Server:    True
Cache Job Environments:      False
-----------------------------------------------------------------
Buildlisted Packages:        None
Skiplisted Packages:         None
-----------------------------------------------------------------
Workspace configuration appears valid.
-----------------------------------------------------------------
```
