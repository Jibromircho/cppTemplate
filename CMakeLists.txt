cmake_minimum_required(VERSION 3.10)
project(OpenGLProject)

set(CMAKE_CXX_STANDARD 17)

# Add include directories
include_directories(${CMAKE_SOURCE_DIR}/include)

# Add source files
set(SOURCES
    src/main.cpp
    src/mysource.cpp
    third_party/glad.c
)

# Add executable
add_executable(OpenGLProject ${SOURCES})

# Link libraries
target_link_libraries(OpenGLProject glfw dl GL)
