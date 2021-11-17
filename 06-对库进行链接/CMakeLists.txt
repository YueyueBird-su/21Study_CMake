cmake_minimum_required(VERSION 3.5)

project(6_demo)

set(
    EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin
)

set(
    SRC_LIST ${PROJECT_SOURCE_DIR}/src/main.cc
)

include_directories(${PROJECT_SOURCE_DIR}/testFunc/inc)

find_library(TESTFUNC_LIB testFunc HINTS ${PROJECT_SOURCE_DIR}/testFunc/lib)

add_executable(main ${SRC_LIST})

target_link_libraries(main ${TESTFUNC_LIB})

# find_library: 在指定目录下查找指定库，并把库的绝对路径存放到变量里，其第一个参数是变量名称，第二个参数是库名称，第三个参数是HINTS，第4个参数是路径，其它用法可以参考cmake文档
# target_link_libraries: 把目标文件与库文件进行链接