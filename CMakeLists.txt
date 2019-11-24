cmake_minimum_required(VERSION 2.8.4)
project(kalman)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(SOURCE_FILES kalman.cpp kalman-test.cpp)
set(EIGEN_INC_DIR /usr/include/eigen3/)

find_package(PythonLibs REQUIRED)
include_directories(${EIGEN_INC_DIR})

add_executable(kalman-test ${SOURCE_FILES})

target_link_libraries(kalman-test ${PYTHON_LIBRARIES})
