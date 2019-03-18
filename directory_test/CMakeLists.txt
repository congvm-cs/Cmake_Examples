cmake_minimum_required(VERSION 2.8)
project(directory_test)

# bring the headers, such as Student.h into the project
include_directories(include)

# Manually add the sources using the set command as follows:
# set(SOURCES src/main.cpp src/Studen.cpp)

# However, the file(GLOB...) allows for wildcard additions
file(GLOB SOURCES "src/*.cpp")

add_executable(testStudent ${SOURCES})


