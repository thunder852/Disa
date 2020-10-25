cmake_minimum_required(VERSION 3.7.2)
project(Disa)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(Vulkan REQUIRED) 
find_package(glfw3 REQUIRED)

include_directories(${Vulkan_INCLUDE_DIRS})

add_subdirectory ("lib/glm")

add_executable(Disa main.cpp)
target_link_libraries(Disa Vulkan::Vulkan glm glfw)