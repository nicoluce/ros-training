cmake_minimum_required(VERSION 2.8.3)
project(robot_description)

find_package(catkin REQUIRED COMPONENTS roslaunch)
roslaunch_add_file_check(launch)
catkin_package()

if(CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
endif()

install(DIRECTORY launch rviz urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
