project(quake)
cmake_minimum_required(VERSION 3.10)

set(CMAKE_C_STANDARD 11)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -Wno-trigraphs -m32 -O0")

include_directories("${CMAKE_SOURCE_DIR}/include")
file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/*.c")
add_executable(quake ${SOURCES})
target_link_libraries(quake "-lX11 -lXext -lm")
