cmake_minimum_required(VERSION 3.16)

project(OpenGL_GLFW3_Glad)
set (SOURCE_FILES src/glad.c)

# Compile the glad source file into a library with the name "glad".
add_library(glad ${SOURCE_FILES})
# Where to find the header files for this library.
target_include_directories(glad PRIVATE include)
