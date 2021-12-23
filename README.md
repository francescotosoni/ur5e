# RoboDK Programs for UR5e

This repo contains some tasks for [UR5e](https://www.universal-robots.com/products/ur5-robot/) in the [ICE lab](https://www.icelab.di.univr.it/) background, from University of Verona. 

In particular, the tasks are: 
- Pick and Place;
- Glue Ceiling path;
- Object Inspection.

Two versions of the pick and place and object inspection have been realized (considered different pick and place positions). 

## Usage

There are three folders in this project: 
- [simulation](/simulation);
- [scripts](/scripts);
- [physical tasks](/physical_tasks).

The programs contained in this repo are developed via [RoboDK](https://robodk.com) software. So, in order to simulate the tasks on the pc environment, the download and installation is required. The object inspection and pick and place tasks are merged in the same [file](simulation/pick_&_place.rdk), while the object inspection is o a separated [one](/simulation/glue_ceiling.rdk). 

However, it is possible to execute the [scripts](/scripts) (`.urp` and `.script` files) directly from the robot teach pendant, transferring the files. The software installation is not required following this execution path. 

Last but not least, the complete [file](/physical_tasks/elaborato.rdk) which contains all the three programs is provided. Use _only this file_ to execute the tasks on the physical robot. Open the project in RoboDK, hit right click on the task in the station and click `"Send program to robot"` option to execute the program on the UR5e. 

:warning: __NOTE__: this scripts are ***only for UR5e robot in the ICE lab***. If you decide to use/execute them in some other context, that is your choice and your responsibility. :warning:

