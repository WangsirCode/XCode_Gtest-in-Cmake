# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)
# 项目信息
project (Demo1)

file(GLOB_RECURSE All_SOURCES  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

add_executable(testMain ${All_SOURCES})

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../src)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../googletest/include)

target_link_libraries(testMain ${CMAKE_CURRENT_SOURCE_DIR}/../src/Debug/libtestlibrary.a)
target_link_libraries(testMain ${CMAKE_CURRENT_SOURCE_DIR}/../googletest/libgtest.a)
