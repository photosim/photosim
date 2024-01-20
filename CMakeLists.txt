cmake_minimum_required(VERSION 3.10)

project(photosim)

file(GLOB SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/source/*.c)

add_executable(photosim ${SOURCES})

add_subdirectory(glfw)
add_subdirectory(cglm)

target_link_libraries(photosim glfw cglm)
