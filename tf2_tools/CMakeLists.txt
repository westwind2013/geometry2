cmake_minimum_required(VERSION 2.8.3)
project(tf2_tools)

find_package(catkin REQUIRED COMPONENTS tf2
                                         tf2_msgs
                                         tf2_ros
)

catkin_package(
   CATKIN_DEPENDS tf2
                  tf2_msgs
                  tf2_ros)

catkin_install_python(PROGRAMS 
  scripts/view_frames.py 
  scripts/echo.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
