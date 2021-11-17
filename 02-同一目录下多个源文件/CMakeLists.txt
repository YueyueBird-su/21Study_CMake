## 法一： 添加所有的文件名
# cmake_minimum_required(VERSION 2.8)

# project(2_demo)

# add_executable(main main.cc testFunc.cc)

## 法二：当文件很多时，指定目录下所有文件存储在一个变量里
cmake_minimum_required(VERSION 2.8)

project(2.1_demo)

# aux_source_directory(dir var)
# 第一个参数dir是指定目录，第二个参数var是用于存放源文件列表的变量

# aux_source_directory(. SRC_LIST)

# aux_source_directory()也存在弊端，
# 它会把指定目录下的所有源文件都加进来，
# 可能会加入一些我们不需要的文件，
# 此时我们可以使用set命令去新建变量来存放需要的源文件
 set( SRC_LIST
     ./main.cc
     ./testFunc.cc
     ./testFunc1.cc
     )

add_executable(main ${SRC_LIST})