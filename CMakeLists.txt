cmake_minimum_required(VERSION 3.0)

find_package(FLEX REQUIRED)
find_package(BISON REQUIRED)

add_library(vmi OBJECT lib.c)
# create libvmi.so
add_library(vmi_shared SHARED $<TARGET_OBJECTS:vmi>)

add_subdirectory(config)
