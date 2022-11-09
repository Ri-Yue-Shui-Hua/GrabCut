cmake_minimum_required(VERSION 3.9)
project(GrabCut VERSION 1.0)
find_package(OpenCV REQUIRED)
##下面是输出信息
message(STATUS "Opnecv ;ibrary status: ")
message(STATUS "> version: ${OpenCV_VERSION} ")
message(STATUS "libraries: ${OpenCV_LIBS} ")
message(STATUS "> include: ${OpenCV_INCLUDE_DIRS}")

include_directories(${OpenCV_INCLUDE_DIRS}) 
file(GLOB SRC_FILES ./*.cpp)
add_executable(GrabCut ${SRC_FILES})
target_link_libraries(GrabCut ${OpenCV_LIBS})
