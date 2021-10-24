cmake_minimum_required(VERSION 3.13.4)

set(CMAKE_CXX_STANDARD 20)

project(json_test)
add_executable(${PROJECT_NAME} source/main.cpp)

add_subdirectory(libjson)