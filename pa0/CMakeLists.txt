cmake_minimum_required (VERSION 2.8.11)
project (Transformation)


include_directories("/opt/homebrew/Cellar/eigen/3.4.0_1/include/eigen3/")

find_package(Eigen3 REQUIRED)
include_directories(EIGEN3_INCLUDE_DIR)

add_executable (Transformation main.cpp)
