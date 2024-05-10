# Minimum CMake version required
cmake_minimum_required(VERSION 3.5)

# Project name
project(opengl-tutorials)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Define sources
set(SOURCES Main.cpp)

# Add an executable target
add_executable(${PROJECT_NAME} ${SOURCES})

# Add shader file to the project
configure_file(Basic.shader Basic.shader COPYONLY)