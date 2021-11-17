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

五 正规一点的组织结构

六 动态库和静态库的编译控制

七 对库进行链接


八 添加编译选项

九 添加控制选项

- CMAKE_SOURCE_DIR: 顶级cmakelists.txt的文件夹目录。
- CMAKE_BINRAY_DIR: 对应cmake的build的目录，主要是运行时生成的文件目录。
- CMAKE_CURRENT_SOURCE_DIR: 一般来说，一个工程会有多个cmakelists.txt文件，对应当前文件目录。
- CMAKE_CURRENT_BINARY_DIR: 对应build里的目录。
- CMAKE_MODULE_PATH: api(include/find_package)包含别的cmake文件时的搜索目录。
- CMAKE_PREFIX_PATH: api(find_libray/path)包含模块时的搜索目录。
- CMAKE_INSTALL_PREFIX: 调用install相关函数，要生成/保存的根目录路径。
