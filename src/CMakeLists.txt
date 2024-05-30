project(planning_main)

#添加两个子目录
add_subdirectory(pnc_map)
add_subdirectory(process)

#把main.cpp添加可执行文件
add_executable(${PROJECT_NAME} planning_main.cpp)

#添加头文件和依赖
target_include_directories(${PROJECT_NAME}#可执行文件用public方式去包含process目录
PUBLIC
${Process_Dir}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
process
)
