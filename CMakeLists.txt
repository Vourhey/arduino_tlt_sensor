cmake_minimum_required(VERSION 2.8.3)
project(arduino_tlt_sensor)

find_package(catkin REQUIRED COMPONENTS
  rospy
)

catkin_package()


## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

catkin_install_python(
    PROGRAMS
        scripts/publish_data
    DESTINATION
        ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(
    FILES
        launch/arduino.launch
    DESTINATION
        ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)


