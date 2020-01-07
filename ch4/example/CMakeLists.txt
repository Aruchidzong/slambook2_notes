find_package(Pangolin REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})


find_package(Sophus REQUIRED)
include_directories(${Sophus_INCLUDE_DIRS})

# Eigen
include_directories("/usr/include/eigen3")
include_directories("/usr/local/include/sophus")
add_executable(trajectoryError trajectoryError.cpp)
target_link_libraries(trajectoryError ${Pangolin_LIBRARIES})
