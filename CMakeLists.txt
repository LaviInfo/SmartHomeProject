cmake_minimum_required(VERSION 2.8.9)
project(SmartHomeProject)

#Bring the headers, such as common.h into the project
include_directories(include)

#Can manually add the sources using the set command as follows:
set(SOURCES src/smho_core.c)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.c")

add_executable(core ${SOURCES})
