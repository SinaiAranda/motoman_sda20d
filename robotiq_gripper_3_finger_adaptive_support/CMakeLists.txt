cmake_minimum_required(VERSION 2.8.3)

project(robotiq_gripper_3_finger_adaptive_support)

find_package(catkin REQUIRED  COMPONENTS
    roscpp
    sensor_msgs
)

catkin_package(
  CATKIN_DEPENDS    
)

find_package(roslaunch)

foreach(dir config launch meshes urdf)
	install(DIRECTORY ${dir}/
		DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach(dir)

include_directories(
include ${catkin_INCLUDE_DIRS}
)
