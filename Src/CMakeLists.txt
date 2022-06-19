# CMakeList.txt: CMakedemo 的 CMake 项目，在此处包括源代码并定义
# 项目特定的逻辑。
#
cmake_minimum_required (VERSION 3.8)

#在CMakeLists.txt中加入头文件搜索路径

INCLUDE_DIRECTORIES(/usr/local/include/hello)


#指定第三方库所在路径，
LINK_DIRECTORIES(/usr/local/lib/)


# 将源代码添加到此项目的可执行文件。
add_executable (CMakedemo "CMakedemo.cpp" "CMakedemo.h")

TARGET_LINK_LIBRARIES(CMakedemo libhello.a)
