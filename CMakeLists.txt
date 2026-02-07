cmake_minimum_required(VERSION 3.30)

project(breakout)

set(target ${PROJECT_NAME})
add_executable(${target})
target_compile_features(${target} PRIVATE cxx_std_26)

find_package(EnTT CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE EnTT::EnTT)
find_package(SDL2 CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE SDL2::SDL2)
find_package(SDL2_image CONFIG REQUIRED)
target_link_libraries(${target} PRIVATE SDL2_image::SDL2_image)

add_subdirectory(src)



