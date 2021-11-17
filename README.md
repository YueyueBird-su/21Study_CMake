# CMake简明教程

> 参考CSDN上的CMake教程：https://blog.csdn.net/whahu1989/article/details/82078563
>
> CMake是开源、跨平台的构建工具，可以让我们通过编写简单的配置文件去生成本地的Makefile，这个配置文件是独立于运行平台和编译器的，这样就不用亲自去编写Makefile了，而且配置文件可以直接拿到其它平台上使用，无需修改，非常方便。

一 安装CMake
我ubuntu20.04，安装cmake使用如下命令，
sudo apt install cmake
安装完成后，在终端下输入cmake -version查看cmake版本，

二 [简单样例](./01-简单样例)

三 [同一目录下多个源文件](./02-同一目录下多个源文件)

四 [不同目录下多个源文件](./03-不同目录下多个源文件)

五 [正规一点的组织结构](./04-正规一点的组织结构)

六 [动态库和静态库的编译控制](./05-动态库和静态库的编译控制)

七 [对库进行链接](./06-对库进行链接)


八 [添加编译选项](./07-添加编译选项)

九 [添加控制选项](./08-添加控制选项)

十 [使用宏添加控制选项](./09-使用宏添加控制选项)

## 常用内置路径

- **CMAKE_SOURCE_DIR**: 顶级cmakelists.txt的文件夹目录。
- **CMAKE_BINRAY_DIR**: 对应cmake的build的目录，主要是运行时生成的文件目录。
- CMAKE_CURRENT_SOURCE_DIR: 一般来说，一个工程会有多个cmakelists.txt文件，对应当前文件目录。
- CMAKE_CURRENT_BINARY_DIR: 对应build里的目录。
- CMAKE_MODULE_PATH: api(include/find_package)包含别的cmake文件时的搜索目录。
- CMAKE_PREFIX_PATH: api(find_libray/path)包含模块时的搜索目录。
- CMAKE_INSTALL_PREFIX: 调用install相关函数，要生成/保存的根目录路径。

## 常用API

- **set** 设置参数，包含一般/缓存/环境变量。
- list 针对列表操作，比如针对文件列表/参数列表/编译列表的增加删除这些。
- file 针对文件操作，如收集文件列表，读写文件等。
- string 针对字符串的操作，如大小写，查找，正则表达式匹配等。
- message 打印消息,可以跟踪测试修改。

------

- add_compile_options：不同平台一般来说有不同的编译设置。
- add_definitions:添加预处理器定义。
- **include_directories**: 如visual studio里的，头文件搜索目录，在当前项目以及当前项目用add_subdirectory添加的项目都会应用。
- target_include_directories：针对指定目标的include_directories。
- **link_libraries**: 添加库文件路径，注意是全路径，如果是本方案的项目，直接使用项目名就行。在当前项目以及当前项目用add_subdirectory添加的项目都会应用。
- **target_link_libraries**：指定目标的link_directories。
- **add_library**：添加库，根据参数生成静态或是动态库。
- **add_executable**：添加执行文件。
- set_target_properties：指定项目一些具体编辑器里的属性，如生成lib/dll的目录。

