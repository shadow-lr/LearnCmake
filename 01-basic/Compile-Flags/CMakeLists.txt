cmake_minimum_required(VERSION 3.8)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DEX2" CACHE STRING "Set C++ Compiler Flags" FORCE)

project(compile_flags)
############################################################
#库的源文件Hello.cpp生成静态库hello_library
add_executable(cmake_examples_compile_flags main.cpp)
# 为可执行文件添加私有编译定义
target_compile_definitions(cmake_examples_compile_flags PRIVATE EX3)