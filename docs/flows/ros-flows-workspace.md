# workspace building flow
This constitutes the main flow of creating a ROS workspace.
```{figure} ../imgs/flows/catkin-flow.png
---
alt: this is a test
align: center
---
diagram showing minimal catkin worspace file hierachy
```

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
    <pre><font color="#4E9A06"><b>fire@fire-box</b></font>:<font color="#3465A4"><b>~/catkin_example_ws</b></font>$ catkin init
    Initializing catkin workspace in `/home/fire/catkin_example_ws`.
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Profile:</font>                     <font color="#C4A000">default</font>
    <font color="#06989A">Extending:</font>             <font color="#4E9A06">[env]</font> <font color="#C4A000">/opt/ros/noetic</font>
    <font color="#06989A">Workspace:</font>                   <font color="#C4A000">/home/fire/catkin_example_ws</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Build Space:</font>       <font color="#CC0000">[missing]</font> <font color="#C4A000">/home/fire/catkin_example_ws/build</font>
    <font color="#06989A">Devel Space:</font>       <font color="#CC0000">[missing]</font> <font color="#C4A000">/home/fire/catkin_example_ws/devel</font>
    <font color="#06989A">Install Space:</font>      <font color="#3465A4">[unused]</font> <font color="#C4A000">/home/fire/catkin_example_ws/install</font>
    <font color="#06989A">Log Space:</font>         <font color="#CC0000">[missing]</font> <font color="#C4A000">/home/fire/catkin_example_ws/logs</font>
    <font color="#06989A">Source Space:</font>       <font color="#4E9A06">[exists]</font> <font color="#C4A000">/home/fire/catkin_example_ws/src</font>
    <font color="#06989A">DESTDIR:</font>            <font color="#3465A4">[unused]</font> <font color="#C4A000">None</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Devel Space Layout:</font>          <font color="#C4A000">linked</font>
    <font color="#06989A">Install Space Layout:</font>        <font color="#C4A000">None</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Additional CMake Args:</font>       <font color="#C4A000">None</font>
    <font color="#06989A">Additional Make Args:</font>        <font color="#C4A000">None</font>
    <font color="#06989A">Additional catkin Make Args:</font> <font color="#C4A000">None</font>
    <font color="#06989A">Internal Make Job Server:</font>    <font color="#C4A000">True</font>
    <font color="#06989A">Cache Job Environments:</font>      <font color="#C4A000">False</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Buildlisted Packages:</font>        <font color="#C4A000">None</font>
    <font color="#06989A">Skiplisted Packages:</font>         <font color="#C4A000">None</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A"><b>Workspace configuration appears valid.</b></font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    </pre>

4.  Build the workspace folder with `catkin build`
    ```bash
    catkin build
    ```
    expected output:
    ```{toggle}
    <pre><font color="#4E9A06"><b>fire@fire-box</b></font>:<font color="#3465A4"><b>~/catkin_example_ws</b></font>$ catkin build
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Profile:</font>                     <font color="#C4A000">default</font>
    <font color="#06989A">Extending:</font>             <font color="#4E9A06">[env]</font> <font color="#C4A000">/opt/ros/noetic</font>
    <font color="#06989A">Workspace:</font>                   <font color="#C4A000">/home/fire/catkin_example_ws</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Build Space:</font>        <font color="#4E9A06">[exists]</font> <font color="#C4A000">/home/fire/catkin_example_ws/build</font>
    <font color="#06989A">Devel Space:</font>        <font color="#4E9A06">[exists]</font> <font color="#C4A000">/home/fire/catkin_example_ws/devel</font>
    <font color="#06989A">Install Space:</font>      <font color="#3465A4">[unused]</font> <font color="#C4A000">/home/fire/catkin_example_ws/install</font>
    <font color="#06989A">Log Space:</font>         <font color="#CC0000">[missing]</font> <font color="#C4A000">/home/fire/catkin_example_ws/logs</font>
    <font color="#06989A">Source Space:</font>       <font color="#4E9A06">[exists]</font> <font color="#C4A000">/home/fire/catkin_example_ws/src</font>
    <font color="#06989A">DESTDIR:</font>            <font color="#3465A4">[unused]</font> <font color="#C4A000">None</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Devel Space Layout:</font>          <font color="#C4A000">linked</font>
    <font color="#06989A">Install Space Layout:</font>        <font color="#C4A000">None</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Additional CMake Args:</font>       <font color="#C4A000">None</font>
    <font color="#06989A">Additional Make Args:</font>        <font color="#C4A000">None</font>
    <font color="#06989A">Additional catkin Make Args:</font> <font color="#C4A000">None</font>
    <font color="#06989A">Internal Make Job Server:</font>    <font color="#C4A000">True</font>
    <font color="#06989A">Cache Job Environments:</font>      <font color="#C4A000">False</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A">Buildlisted Packages:</font>        <font color="#C4A000">None</font>
    <font color="#06989A">Skiplisted Packages:</font>         <font color="#C4A000">None</font>
    <font color="#75507B">-----------------------------------------------------------------</font>
    <font color="#06989A"><b>Workspace configuration appears valid.</b></font>

    <font color="#06989A"><b>NOTE:</b></font> Forcing CMake to run for each package.
    <font color="#75507B">-----------------------------------------------------------------</font>
    [build] No packages were found in the source space &apos;/home/fire/catkin_example_ws/src&apos;
    [build] No packages to be built.
    [build] Package table is up to date.                                                                                                   
    Starting  <font color="#4E9A06"><b>&gt;&gt;&gt;</b></font> <font color="#06989A"><b>catkin_tools_prebuild               </b></font>                                                                                     
    <font color="#2E3436"><b>Finished</b></font>  <font color="#4E9A06">&lt;&lt;&lt;</font> <font color="#06989A">catkin_tools_prebuild               </font> [ <font color="#C4A000">1.8 seconds</font> ]                                                                     
    [build] <font color="#4E9A06"><i><b>Summary:</b></i></font> <i>All </i><i><b>1</b></i> <i>packages succeeded!</i>                                                                                             
    [build]   <font color="#2E3436"><i><b>Ignored:   None.</b></i></font>                                                                                                             
    [build]   <font color="#2E3436"><i><b>Warnings:  None.</b></i></font>                                                                                                             
    [build]   <font color="#2E3436"><i><b>Abandoned: None.</b></i></font>                                                                                                             
    [build]   <font color="#2E3436"><i><b>Failed:    None.</b></i></font>                                                                                                             
    [build] <i><b>Runtime:</b></i> <i>1.8 seconds total.</i> </pre>

### Summary 

```{figure} ../imgs/itaintmuch.jpg
---
align: center
height: 350
width: 350
---
``` 
we have finished building an empty ROS workspace, which is the first of building a robot with ROS
our file structure should look like this:


 in the next guides we will build packages **inside** this workspace.