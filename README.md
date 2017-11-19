Setup:

To compile the packages you need to have also map_server, costmap_2d ROS packages ?and install yaml-cpp available at https://github.com/jbeder/yaml-cpp?.

Parameters:

Additionally to the original GMapping parameters, two extra parameters are introduced. 
The "yaml" parameter contains a path of the .yaml file. If nothing is provided GMapping runs without prior map.
The "map_trust" parameter which expresses how reliable the prior map is. Higher the number is, harder it will be for the robot to erase given map.

YAML:

Elements of the .yaml file are the same as in AMCL case.

(From http://wiki.ros.org/map_server)
image : Path to the image file containing the occupancy data; can be absolute, or relative to the location of the YAML file
resolution : Resolution of the map, meters / pixel
origin : The 2-D pose of the lower-left pixel in the map, as (x, y, yaw), with yaw as counterclockwise rotation (yaw=0 means no rotation). Many parts of the system currently ignore yaw.
occupied_thresh : Pixels with occupancy probability greater than this threshold are considered completely occupied.
free_thresh : Pixels with occupancy probability less than this threshold are considered completely free.
negate : Whether the white/black free/occupied semantics should be reversed (interpretation of thresholds is unaffected) 

Examples:

Try the modified version of GMapping with launch file in Examples folder.
