cmake_minimum_required(VERSION 4.0)
project(VulkanPlayground)

set(CMAKE_CXX_STANDARD 20)

# Find Vulkan
find_package(Vulkan REQUIRED)

# Find or download GLFW
find_package(glfw3 CONFIG REQUIRED)

add_executable(VulkanPlayground src/main.cpp)

# Link libraries
target_link_libraries(VulkanPlayground PRIVATE
        Vulkan::Vulkan
        glfw
)