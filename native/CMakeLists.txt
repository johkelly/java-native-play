cmake_minimum_required(VERSION 3.2)
project (example)
include_directories("${PROJECT_BINARY_DIR}" src)

add_library(example SHARED example.cpp)
add_executable(runner runner.cpp)
target_link_libraries(runner example)
