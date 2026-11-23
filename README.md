# Autonomous Rescue Robot with TurtleBot

ROS 1 catkin workspace for the EECE 5550 final project. Start with the [source tree](src) for package manifests, launch files, and robot code.

For a local rebuild, copy the source into a clean workspace, resolve dependencies for your ROS 1 distribution, and build there. The checked-in build outputs may reference paths from the original machine. Check launch configuration against your TurtleBot and sensor setup before operating hardware.

## Navigation package

`src/my_nav/launch/exploration.launch` combines AMCL, `move_base`, and `explore_lite`. It accepts a TurtleBot3 model plus velocity and odometry topic arguments. A simulation or robot bringup must provide the expected map, scan, odometry, and TF data. Source the clean catkin workspace, then inspect the launch with `roslaunch --nodes my_nav exploration.launch model:=burger` after installing its dependencies. Verify the expected nodes and topic names in simulation before a hardware run.
