cmake_minimum_required(VERSION 3.3 FATAL_ERROR)

project(OpenGL2D)

add_executable(OpenGL2D src/main.cpp src/main)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(OpenGL2D glfw)

add_subdirectory(external/glad)
target_link_libraries(OpenGL2D glad)