cmake_minimum_required(VERSION 4.3)
project(OpenGLLoader LANGUAGES C)

set(CMAKE_C_STANDARD 23)

add_library(OpenGLLoader STATIC src/glad.c)
target_include_directories(OpenGLLoader PUBLIC include)