cmake_minimum_required(VERSION 3.10)
project(clapTest)
set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/winx64.cmake")
set(LIBRARY_NAME clapTest)

set(LIBRARY_OUTPUT_PATH ${CMAKE_CURRENT_SOURCE_DIR}/out/)

#add_executable(clapTest plugin.c)
add_library(clapTest SHARED plugin.c)

add_definitions(-DUNICODE -D_UNICODE)
target_include_directories(clapTest PRIVATE include/)

