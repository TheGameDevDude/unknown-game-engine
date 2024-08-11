cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(unknown-game-engine VERSION 1.0)

add_executable(unknown-game-engine main.cpp glad.c)

# include all the headers
set(INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/dependencies/include)
include_directories(${INCLUDE_DIR})

# linking all the libraries
set(GLFW_LIBRARY_PATH ${CMAKE_CURRENT_SOURCE_DIR}/dependencies/lib/libglfw3.a)
target_link_libraries(unknown-game-engine ${GLFW_LIBRARY_PATH})