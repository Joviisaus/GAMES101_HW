cmake_minimum_required(VERSION 3.10)
project(RayTracing)

include_directories("/opt/homebrew/Cellar/eigen/3.4.0_1/include/")
include_directories("/opt/homebrew/Cellar/opencv/4.7.0_4/include/opencv4/")


set(CMAKE_CXX_STANDARD 17)

add_executable(RayTracing main.cpp Object.hpp Vector.hpp Sphere.hpp global.hpp Triangle.hpp Scene.cpp Scene.hpp Light.hpp Renderer.cpp)
target_compile_options(RayTracing PUBLIC -Wall -Wextra -pedantic -Wshadow -Wreturn-type -fsanitize=undefined)
target_compile_features(RayTracing PUBLIC cxx_std_17)
target_link_libraries(RayTracing PUBLIC -fsanitize=undefined)
