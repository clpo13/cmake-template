cmake_minimum_required(VERSION 3.0)

project(cmake-template
        VERSION 0.1.0
        LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
enable_testing()

configure_file(${CMAKE_SOURCE_DIR}/config.h.in ${CMAKE_CURRENT_BINARY_DIR}/config.h)
include_directories(${CMAKE_CURRENT_BINARY_DIR})

add_subdirectory(src)
