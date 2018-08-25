# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)
# 项目信息
project (Demo)

file(GLOB_RECURSE All_SOURCES  ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

set(CMAKE_MACOSX_RPATH 1)

add_library(testlibrary ${All_SOURCES})

include_directories(${CMAKE_CURRENT_SOURCE_DIR})