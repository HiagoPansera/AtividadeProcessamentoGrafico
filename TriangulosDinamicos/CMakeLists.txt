cmake_minimum_required(VERSION 3.0)
project(TriangulosDinamicos)

set(CMAKE_CXX_STANDARD 11)

add_executable(TriangulosDinamicos src/main.cpp)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS} ${GLFW_INCLUDE_DIRS} include)

target_link_libraries(TriangulosDinamicos ${OPENGL_LIBRARIES} glfw glad)
