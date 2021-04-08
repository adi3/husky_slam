cmake_minimum_required(VERSION 3.0.2)
project(husky_exploration)

find_package(catkin REQUIRED
  husky_gazebo
  husky_navigation
  husky_viz
)


###################################
## catkin specific configuration ##
###################################
## The catkin_package macro generates cmake config files for your package
## Declare things to be passed to dependent projects
## INCLUDE_DIRS: uncomment this if your package contains header files
## LIBRARIES: libraries you create in this project that dependent projects also need
## CATKIN_DEPENDS: catkin_packages dependent projects also need
## DEPENDS: system dependencies of this project that dependent projects also need
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES husky_exp
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
 ${catkin_INCLUDE_DIRS}
)

install(
  DIRECTORY launch rviz maps config
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
