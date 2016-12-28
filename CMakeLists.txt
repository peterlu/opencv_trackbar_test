cmake_minimum_required(VERSION 3.0)

project(opencv_tests)

set(CMAKE_CXX_FLAGS "-std=c++11 -Wall")

include_directories(${CMAKE_CURRENT_SOURCE_DIR}
					/usr/local/include)

set(SOURCES trackbar.cpp)

add_executable(trackbar ${SOURCES})

target_link_libraries(trackbar LINK_PUBLIC 
									opencv_core
									opencv_imgproc
									opencv_highgui
									opencv_imgcodecs)

