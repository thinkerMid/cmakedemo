# CMakeList.txt: 顶层 CMake 项目文件，在此处执行全局配置
# 并包含子项目。
#
cmake_minimum_required (VERSION 3.8)

project ("CMakedemo")

#包含子项目 指定中间二进制和目标二进制存放的位置
add_subdirectory ("Src" "bin") 
#add_subdirectory ("lib" "bin")#编译动态库时取消这个注释 将上一行注释 
INSTALL(FILES COPYRIGHT README DESTINATION share/doc/cmake)
INSTALL(PROGRAMS runhello.sh DESTINATION bin)
INSTALL(DIRECTORY doc/ DESTINATION share/doc/cmake)




