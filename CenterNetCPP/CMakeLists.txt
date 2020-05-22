cmake_minimum_required(VERSION 2.8.8)

project (centernet)

find_package(Caffe)
include_directories(${Caffe_INCLUDE_DIRS})
add_definitions(${Caffe_DEFINITIONS})

add_executable(centernet centernet.cpp)
target_link_libraries(centernet ${Caffe_LIBRARIES})
