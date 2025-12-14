cmake_minimum_required(VERSION 3.20.0)

project(OpenGLProject LANGUAGES C CXX)
set(CMAKE_CXX_STANDARD 20)

include(CTest)
enable_testing()

add_executable(app
    src/main.cpp
    src/test.cpp
    src/glad.c
    )

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(app PRIVATE glfw)


target_include_directories(app PRIVATE include)