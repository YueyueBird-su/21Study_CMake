cmake_minimum_required(VERSION 2.8)

project(3_demo)

# 向工程添加多个指定头文件的搜索路径，路径之间用空格分隔。
include_directories(testFunc testFunc1)

aux_source_directory(testFunc SRC_LIST)
aux_source_directory(testFunc1 SRC_LIST1)

add_executable(main main.cc ${SRC_LIST} ${SRC_LIST1})