project(process)

#添加动态库(把。cpp文件添加动态库)
add_library(${PROJECT_NAME}
SHARED
process.cpp
)

target_include_directories(${PROJECT_NAME}
PUBLIC
${PNC_Map_Dir}
)

target_link_libraries(${PROJECT_NAME}
PUBLIC
pnc_map
)