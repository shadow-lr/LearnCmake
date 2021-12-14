# CMakeList.txt: LearnCmake-Vs 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.8)

# Setup vcpkg script with CMake (note: should be placed before project() call)
set(CMAKE_TOOLCHAIN_FILE D:/repos/vcpkg-master/scripts/buildsystems/vcpkg.cmake CACHE STRING "Vcpkg toolchain file")

project("LearnCmake-Vs")
add_executable(${PROJECT_NAME} LearnCmake-Vs.cpp)
