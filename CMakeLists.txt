cmake_minimum_required(VERSION 3.23.0)
project(planning#工程命名
    VERSION 0.0.1#工程版本
    DESCRIPTION "a demo of cmake planning"
    HOMEPAGE_URL "https://github.com/iflytekruimin/cmake_planning_demo"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)

#变量设置
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)#设置动态库和可执行文件的输出目录，同时设置的变量会传到子目录里面，
#子目录里面的cmakelist也是可以用到父目录里的变量，相当于C++里面的类与类之间的继承
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)

#添加子目录
add_subdirectory(src)#找子目录里面的cmakelist