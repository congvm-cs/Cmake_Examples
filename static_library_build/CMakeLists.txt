cmake_minimum_required(VERSION 2.8)
project(shared_library_test)
set(CMAKE_BUILD_TYPE Release)


# bring the headers, such as Student.h into the project
include_directories(include)

# Manually add the sources using the set command as follows:
# set(SOURCES src/main.cpp src/Studen.cpp)

# However, the file(GLOB...) allows for wildcard additions
file(GLOB SOURCES "src/*.cpp")

add_library(testStudent STATIC ${SOURCES})

# Set the location for library installation -- ie. /usr/lib
# in this case not really necessary in this example. Use
# `sudo make install` to apply
install(TARGETS testStudent DESTINATION /usr/lib)
