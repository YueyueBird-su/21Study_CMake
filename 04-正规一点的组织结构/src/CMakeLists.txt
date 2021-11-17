aux_source_directory(. SRC_LIST)

include_directories(../include)

add_executable(main ${SRC_LIST})

set(
    EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin
)

# set: 用于定义变量
# EXECUTABLE_OUTPUT_PATH ：目标二进制可执行文件的存放位置
# PROJECT_SOURCE_DIR：工程的根目录