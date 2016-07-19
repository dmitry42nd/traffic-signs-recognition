cmake_minimum_required(VERSION 3.5)
project(cogent_embedded)

find_package(OpenCV 3.1 REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES src/main.cpp)
add_executable(cogent_embedded ${SOURCE_FILES})

target_link_libraries(cogent_embedded ${OpenCV_LIBS})