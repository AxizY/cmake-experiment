cmake_minimum_required(VERSION 3.10)

project(Triangle)
find_package(glfw3 REQUIRED)

add_executable(Triangle main.cpp)
target_link_libraries(Triangle glfw)
if (APPLE)
  target_link_libraries(Triangle "-framework OpenGL")
endif()
