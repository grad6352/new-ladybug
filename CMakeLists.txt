cmake_minimum_required(VERSION 3.13)

project(my_app)

set(AFR_BOARD espressif.esp32_devkitc CACHE INTERNAL "")
add_subdirectory(amazon-freertos)

add_subdirectory(my_app/main.c)
target_link_libraries(my_app PRIVATE AFR::mqtt)