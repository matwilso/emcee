cmake_minimum_required(VERSION 2.8.3)
project(emcee_control)

find_package(catkin REQUIRED COMPONENTS
	roscpp
	joy
	geometry_msgs
	sensor_msgs
	control_msgs
	rosconsole
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES emcee_control
#  CATKIN_DEPENDS ros_control ros_controllers
#  DEPENDS system_lib
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

## Declare a C++ executable
add_executable(joy_teleop src/joy_teleop.cpp)
target_link_libraries(joy_teleop ${catkin_LIBRARIES})
