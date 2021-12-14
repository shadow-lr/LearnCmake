cmake_minimum_required (VERSION 3.8)

project(hello_headers)

set(SOURCES
    src/Hello.cpp
    src/main.cpp)

add_executable(${PROJECT_NAME} ${SOURCES})

#设置这个可执行文件hello_headers需要包含的库的路径
target_include_directories(${PROJECT_NAME} PRIVATE ${PROJECT_SOURCE_DIR}/include)

#PROJECT_SOURCE_DIR指工程顶层目录
#PROJECT_Binary_DIR指编译目录