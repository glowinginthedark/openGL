cmake_minimum_required(VERSION 3.8)
project(main LANGUAGES C CXX)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/CMake/Modules/")

find_package(glfw3 REQUIRED)


set(EXT_SOURCE_DIR "/path/to/glad/src")
set(EXT_INCLUDE_DIR "/path/to/glad/include/glad")
add_library(glad "${EXT_INCLUDE_DIR}/glad.h" "${EXT_SOURCE_DIR}/glad.c")
target_include_directories(glad PUBLIC ${EXT_INCLUDE_DIR})


add_executable(${PROJECT_NAME} "${CMAKE_SOURCE_DIR}/main.cpp")


target_link_libraries(${PROJECT_NAME} PUBLIC glfw glad PRIVATE ${CMAKE_DL_LIBS})
