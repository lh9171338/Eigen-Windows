########### 设置版本
cmake_minimum_required(VERSION 3.20)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_BUILD_TYPE Debug)
message(STATUS "Build Type: ${CMAKE_BUILD_TYPE}")

########### 设置项目名称
project(eigen_demo)

########### 添加库
# eigen
find_package(EIGEN3 REQUIRED)
include_directories(${EIGEN3_INCLUDE_DIRS})
message(STATUS "EIGEN3_INCLUDE_DIRS: ${EIGEN3_INCLUDE_DIRS}")

########### 编译可执行文件
add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME})
