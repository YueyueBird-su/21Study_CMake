# 把源文件放到src目录下，
# 把头文件放入到include文件下，
# 生成的对象文件放入到build目录下，
# 最终输出的elf文件会放到bin目录下

cmake_minimum_required(VERSION 2.8)

project(4_demo)

# 向当前工程添加存放源文件的子目录，并可以指定中间二进制和目标二进制的存放位置
# 这里指定src目录下存放了源文件，
# 当执行cmake时，就会进入src目录下去找src目录下的CMakeLists.txt，
# 所以在src目录下也建立一个CMakeLists.txt
add_subdirectory(src)

# 如果只有外层一个cmakelists的情况，也可以直接：
# cmake_minimum_required (VERSION 2.8)
# 
# project (demo)
# 
# set (EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
# 
# aux_source_directory (src SRC_LIST)
# 
# include_directories (include)
# 
# add_executable (main ${SRC_LIST})
