cmake_minimum_required(VERSION 3.10)
project(Bridge LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(Bridge SHARED Bridge.cpp)

if(WIN32)
    target_link_libraries(Bridge user32 gdi32)
endif()
