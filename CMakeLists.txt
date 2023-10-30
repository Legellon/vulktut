cmake_minimum_required(VERSION 3.13.4)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

include_directories("/usr/local/include")

set(ENV{VK_ICD_FILENAMES} "/usr/local/share/vulkan/icd.d/MoltenVK_icd.json")
set(ENV{VK_LAYER_PATH} "/usr/local/share/vulkan/explicit_layer.d/")

# set the project name
project(vulktut)

# add the executable
add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} "/usr/local/lib/libglfw.3.3.dylib")
target_link_libraries(${PROJECT_NAME} "/usr/local/lib/libvulkan.1.dylib")
target_link_libraries(${PROJECT_NAME} "/usr/local/lib/libvulkan.1.3.224.dylib")
