# RoboDK Programs for UR5e

This repo contains some tasks for [UR5e](https://www.universal-robots.com/products/ur5-robot/) in the [ICE lab](https://www.icelab.di.univr.it/) background, from University of Verona. 

In particular, the tasks are: 
- Pick and Place;
- Glue Ceiling path;
- Object Inspection.

Two versions of the pick and place and object inspection have been realized (considered different pick and place positions). 

## Technical Details

Joint moves (MoveJ) are used for the larger moves, while linear moves (MoveL) are used only when maintaining more precise trajectories (glue ceiling task and pick move after approach place movement after place move).

In order to define robot targets, __three reference frames__ have been realized: one for each bay and one near the camera. Starting from those, the various targets useful for each task have been defined. An approach target has been set for each bay, then the robot can proceed with the approach to the position of the lego block (pick and place and object inspection) or to the first point of trajectory (glue ceiling). By doing this, we avoid making movements that are dangerous to the surrounding environment and to the robot itself. 

In the projects there are two versions of pick and place and object inspection: they differ in the bay of departure and arrival (I identify as Bay 1 the one in front of the robot and Bay 2 the one closer to the camera setting). 

![ICE_lab_sim](https://user-images.githubusercontent.com/39372510/147255903-a3d13f86-5f91-41c8-922a-50614133d429.jpg)

The glue ceiling instead is performed only at Bay 1, following an "M" trajectory. 

## Usage

There are three folders in this project: 
- [simulation](/simulation);
- [scripts](/scripts);
- [physical tasks](/physical_tasks).

The programs contained in this repo are developed via [RoboDK](https://robodk.com) software. So, in order to simulate the tasks on the pc environment, the download and installation is required. The object inspection and pick and place tasks are merged in the same [file](simulation/pick_&_place.rdk), while the object inspection is o a separated [one](/simulation/glue_ceiling.rdk). 

However, it is possible to execute the [scripts](/scripts) (`.urp` and `.script` files) directly from the robot teach pendant, transferring the files. The software installation is not required following this execution path. 

Last but not least, the complete [file](/physical_tasks/elaborato.rdk) which contains all the three programs is provided. Use _only this file_ to execute the tasks on the physical robot. Open the project in RoboDK, hit right click on the task in the station and click `"Send program to robot"` option to execute the program on the UR5e. 

![ICE_lab](https://user-images.githubusercontent.com/39372510/147258168-030011b7-3957-47f3-a077-07071058f162.jpg)

 __NOTE__: to obtain the maximum fluidity in the movements it is recommended the use of offline programming, while pick n place and object inspection can be performed only offline because of the gripper control. 

:warning: __NOTE__: execute these scripts ***only on UR5e robot in the ICE lab***. :warning:

