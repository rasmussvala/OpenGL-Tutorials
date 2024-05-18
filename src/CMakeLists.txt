# Minimum CMake version required
cmake_minimum_required(VERSION 3.5)

# Project name
project(opengl-tutorials)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Define sources
set(SOURCES
    Main.cpp
    Basic.shader 
)

# Add an executable target
add_executable(${PROJECT_NAME} ${SOURCES})

# Set properties for shader files to make sure they are not compiled
set_source_files_properties(Basic.shader PROPERTIES HEADER_FILE_ONLY TRUE)
