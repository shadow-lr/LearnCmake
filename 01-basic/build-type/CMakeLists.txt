cmake_minimum_required(VERSION 3.8)

# 如果没有指定则设置默认编译方式
if (NOT CMAKE_BUILD_TYPE AND NOT CMAKE_CONFIGURATION_TYPES)
    # 在命令行中输出message里的信息
    message("Setting build type to 'RelWithDebInfo' as none was specified")
    # 不管CACHE里有没有设置过CMAKE_BUILD_TYPE这个变量，都强制赋值这个值为RelWithDebInfo
    set(CMAKE_BUILD_TYPE RealWithDebInfo CACHE STRING "Choose the type of build." FORCE)

    set_property(CACHE CMAKE_BUILD_TYPE PROPERTY STRINGS "Debug" "Release" "MinSizeRel" "RealWithDebInfo")

endif()

project(build_type)
############################################################
#库的源文件Hello.cpp生成静态库hello_library
add_executable(cmake_examples_build_type main.cpp)