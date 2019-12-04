cmake_minimum_required(VERSION 2.8.4)
project(kalman)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(SOURCE_FILES kalman.cpp kalman-test.cpp)

find_package(Eigen3 REQUIRED)
message("Eigen3-PATH:${EIGEN3_INCLUDE_DIR}")
include_directories(${EIGEN3_INCLUDE_DIRS})

find_package(PythonLibs 2.7  REQUIRED)
message("Python-PATH:${PYTHON_LIBRARIES}")

add_executable(kalman-test ${SOURCE_FILES})

target_link_libraries(kalman-test ${PYTHON_LIBRARIES})
#target_link_libraries(kalman-test /usr/lib/x86_64-linux-gnu/libpython2.7.so)
