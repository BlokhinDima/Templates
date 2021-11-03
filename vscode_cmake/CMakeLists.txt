# CMake required version
cmake_minimum_required(VERSION 3.2)

# Project name
project(Study)

# Directories
set(SRC_DIR "source/")
set(INC_DIR "inc/")

add_executable(Study ${SRC_DIR}main.cpp)
