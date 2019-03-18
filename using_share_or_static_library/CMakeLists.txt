cmake_minimum_required(VERSION 2.8)
project(use_shared_lib)

# For the shared library:
set(PROJECT_LINK_LIBS libtestStudent.so)
link_directories(/home/vmc/Workspaces/Cpp_Cmake/shared_library_build/build/) # path to .so file

# For the static library
# set(PROJECT_LINK_LIBS libtestStudent.a)
link_directories(/home/vmc/Workspaces/Cpp_Cmake/static_library_build/build)


# Need include "include directory from shared library"
include_directories(/home/vmc/Workspaces/Cpp_Cmake/shared_library_build/include/)

# Set executable
add_executable(test_use_shared_lib main.cpp)

# link executable to shared library
target_link_libraries(test_use_shared_lib ${PROJECT_LINK_LIBS})