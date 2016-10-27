cmake_minimum_required(VERSION 3.6)


project(HelloWorld)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# Where to find CMake modules and OpenCV
set(OpenCV_DIR "C:\\cygwin64\\home\\cobalt\\src\\opencv-3.1.0\\build")
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")

find_package(OpenCV REQUIRED)
#include_directories(${OpenCV_INCLUDE_DIRS})
#link_directories("C:\\cygwin64\\usr\\local\\opencv-3.1.0\\bin")

add_executable(HelloWorld main.cpp)

# add libs you need
set(OpenCV_LIBS opencv_core opencv_imgcodecs opencv_highgui )

# linking
target_link_libraries(HelloWorld ${OpenCV_LIBS})