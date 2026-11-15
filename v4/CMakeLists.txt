#使用动态库文件
cmake_minimum_required(VERSION 3.15)
project(test)
file(GLOB SRC ${PROJECT_SOURCE_DIR}/*.cpp)#依旧搜索cpp
#set(EXECUTABLE_OUTPUT_PATH /home/xj/praCMAKE/v1)                                                                                                                                                                    
set(CMAKE_CXX_STANDARD 11)                       
include_directories(${PROJECT_SOURCE_DIR}/include)#有子目录时需要指定出头文件所在文件夹                                                                                                                                                                                                                                                                                                              
link_directories(${PROJECT_SOURCE_DIR}/lib2)#指定动态库路径，否则找不到
add_executable(app ${SRC})
target_link_libraries(app calc)#这行一般放在最后，生成可执行文件之后再调用
