# RoboDK Programs for UR5e

This repo contains some tasks for UR5e in the ICE lab background, from University of Verona. 

In particular, the tasks are: 
- Pick and Place;
- Glue Ceiling path;
- Object Inspection.

Two versions of the pick and place and object inspection have been realized (considered different pick and place positions). 

## Usage

The programs contained in this repo are developed via [RoboDK](https://robodk.com) software. So, in order to use the ones in the [simulation](/simulation) folder (specially for online programming), the download and installation is required. The object inspection is merged in the pick and place file. 

However, it is possible to execute the scripts (`.urp` and `.script` files) directly from the robot teach pendant. These files are contained in [scripts](/scripts) folder. 

Last but not least, the complete [file](/physical_tasks/elaborato.rdk) which contains all the three programs is provided. Use _only this file_ to execute the tasks on the physical robot. Hit right click on the task in the station and click `"Send program to robot"` option to execute the program on the UR5e. 

:warning: __NOTE__: this scripts are ***only for UR5e robot in the ICE lab***. If you decide to use/execute them in some other context, that is your choice and your responsibility. :warning:
