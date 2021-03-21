################################################################################
# Set minimum required version of cmake, project name and compile options
################################################################################
cmake_minimum_required(VERSION 3.0.2)
project(launchfile_switcher)

################################################################################
# Find catkin packages and libraries for catkin and system dependencies
################################################################################
find_package(catkin REQUIRED COMPONENTS
  rospy
  roslaunch
  rosnode
)

################################################################################
# Setup for python modules and scripts
################################################################################
catkin_python_setup()

################################################
## Declare ROS dynamic reconfigure parameters ##
################################################


###################################
## catkin specific configuration ##
###################################


###########
## Build ##
###########
catkin_package(
  CATKIN_DEPENDS rospy roslaunch rosnode
)

## Specify additional locations of header files
## Your package locations should be listed before other locations

#############
## Install ##
#############
catkin_install_python(PROGRAMS 
  nodes/launchfile_switcher
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

#############
## Testing ##
#############

