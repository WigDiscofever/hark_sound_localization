# Catkin User Guide: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/user_guide.html
# Catkin CMake Standard: http://www.ros.org/doc/groovy/api/catkin/html/user_guide/standards.html
cmake_minimum_required(VERSION 2.8.3)
project(hark_msgs)
# Load catkin and all dependencies required for this package
# TODO: remove all from COMPONENTS that are not catkin packages.
find_package(catkin REQUIRED COMPONENTS roscpp roslib rospy message_generation)

# include_directories(include ${Boost_INCLUDE_DIR} ${catkin_INCLUDE_DIRS})
# CATKIN_MIGRATION: removed during catkin migration
# cmake_minimum_required(VERSION 2.4.6)

# CATKIN_MIGRATION: removed during catkin migration
# include($ENV{ROS_ROOT}/core/rosbuild/rosbuild.cmake)

# Set the build type.  Options are:
#  Coverage       : w/ debug symbols, w/o optimization, w/ code-coverage
#  Debug          : w/ debug symbols, w/o optimization
#  Release        : w/o debug symbols, w/ optimization
#  RelWithDebInfo : w/ debug symbols, w/ optimization
#  MinSizeRel     : w/o debug symbols, w/ optimization, stripped binaries
#set(ROS_BUILD_TYPE RelWithDebInfo)


# CATKIN_MIGRATION: removed during catkin migration
# rosbuild_init()

#set the default path for built executables to the "bin" directory
#set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
#set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

#uncomment if you have defined messages
add_message_files(
  FILES
  HarkFeature.msg
  HarkFeatureVal.msg
  HarkFFT.msg
  HarkFFTVal.msg
  HarkInt.msg
  HarkJulius.msg
  HarkJuliusSrc.msg
  HarkJuliusSrcVal.msg
  HarkSource.msg
  HarkSourceVal.msg
  HarkSrcFeature.msg
  HarkSrcFeatureMFM.msg
  HarkSrcFeatureMFMVal.msg
  HarkSrcFeatureVal.msg
  HarkSrcFFT.msg
  HarkSrcFFTVal.msg
  HarkSrcWave.msg
  HarkSrcWaveVal.msg
  HarkWave.msg
  HarkWaveVal.msg
  promxy.msg
)
#uncomment if you have defined services
add_service_files(
  FILES
  HarkIntSrv.srv
)

#common commands for building c++ executables and libraries
#add_library(${PROJECT_NAME} src/example.cpp)
#target_link_libraries(${PROJECT_NAME} another_library)
#
# CATKIN_MIGRATION: removed during catkin migration
# rosbuild_add_boost_directories()
#find_package(Boost REQUIRED COMPONENTS thread)
#include_directories(${Boost_INCLUDE_DIRS})
#target_link_libraries(${PROJECT_NAME} ${Boost_LIBRARIES})
#add_executable(example examples/example.cpp)
#target_link_libraries(example ${PROJECT_NAME})
## Generate added messages and services with any dependencies listed here
generate_messages(
    DEPENDENCIES std_msgs
)

# catkin_package parameters: http://ros.org/doc/groovy/api/catkin/html/dev_guide/generated_cmake_api.html#catkin-package
# TODO: fill in what other packages will need to use this package
#catkin_package(
#    DEPENDS roscpp roslib rospy
#    CATKIN_DEPENDS # TODO
#    INCLUDE_DIRS # TODO include
#    LIBRARIES # TODO
#)
