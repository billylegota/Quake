project(quake)
cmake_minimum_required(VERSION 3.10)

set(CMAKE_C_STANDARD 90)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -m32 -O0")

file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "WinQuake/*.c")
add_executable(quake ${SOURCES})
target_link_libraries(quake "-lX11 -lXext -lm")
