cmake_minimum_required(VERSION 3.13.4)

set(CMAKE_CXX_STANDARD 20)

project(json_test)
add_executable(${PROJECT_NAME} source/main.cpp)

add_subdirectory(libutilities)
add_subdirectory(libjson)

get_target_property(LIBJSON_INCLUDE_DIRECTORIES libjson INCLUDE_DIRECTORIES)

message(${LIBJSON_INCLUDE_DIRECTORIES})
target_include_directories(${PROJECT_NAME} PRIVATE ${LIBJSON_INCLUDE_DIRECTORIES})