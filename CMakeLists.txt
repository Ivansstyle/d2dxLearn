cmake_minimum_required(VERSION 3.23)
project(d2dxLearn)

if(!WIN32)
    message(FATAL_ERROR "This project can only be run on windows.")
endif()

set(CMAKE_CXX_STANDARD 17)


# For CMake to link against WIN32 libraries and accept WIN32 specific C++ methods, WIN32 must be mentioned in add_executable
# https://cmake.org/cmake/help/v3.8/command/add_executable.html
# WinMain() becomes an entry point and program becomes a GUI executable
# https://cmake.org/cmake/help/v3.8/prop_tgt/WIN32_EXECUTABLE.html#prop_tgt:WIN32_EXECUTABLE
add_executable(d2dxLearn WIN32 main.cpp)

