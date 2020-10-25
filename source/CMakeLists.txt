cmake_minimum_required(VERSION 3.7.2)
project(Disa)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Find packages in the OS
find_package(Vulkan REQUIRED) 
find_package(glfw3 REQUIRED)

# Add sub_directories/s
add_subdirectory ("${PROJECT_SOURCE_DIR}/libVendor/glm/glm")

# Add include directories
include_directories ("${PROJECT_SOURCE_DIR}/libVendor/stb")
include_directories(${Vulkan_INCLUDE_DIRS})

add_executable(Disa main.cpp)
target_link_libraries(Disa Vulkan::Vulkan glm glfw)