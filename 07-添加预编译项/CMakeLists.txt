cmake_minimum_required(VERSION 2.8)

project(7_demo)

set(
    EXECUTABLE_OUTPUT_PATH
    ${PROJECT_SOURCE_DIR}/bin
)

add_compile_options(-std=c++11 -Wall)

add_executable(main main.cc)