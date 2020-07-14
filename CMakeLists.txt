cmake_minimum_required(VERSION 3.16)
project(OpenGL_SDL2)

set(CMAKE_CXX_STANDARD 14)
set (SOURCE_FILES main.cpp)
add_executable(${PROJECT_NAME} ${SOURCE_FILES})

# Add glad to project.
add_subdirectory(glad)
target_include_directories(glad PRIVATE glad/include)
target_link_libraries(${PROJECT_NAME} "glad" "${CMAKE_DL_LIBS}")

# Add SDL2 to project.
add_subdirectory(SDL2)
target_include_directories(${PROJECT_NAME} PRIVATE ${SDL2_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} SDL2 ${SDL2_LIBRARIES})

