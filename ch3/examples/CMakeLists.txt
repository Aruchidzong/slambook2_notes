cmake_minimum_required(VERSION 3.5)
project(example)

SET(CMAKE_CXX_FLAGS "-std=c++0x")
include_directories("/usr/include/eigen3")
add_executable(coordinateTransform coordinateTransform.cpp)



cmake_policy(SET CMP0003 NEW)
find_package(Pangolin REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})
add_executable(plotTrajectory plotTrajectory.cpp)
target_link_libraries(plotTrajectory ${Pangolin_LIBRARIES})
