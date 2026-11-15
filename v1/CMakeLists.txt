cmake_minimum_required(VERSION 3.15)
project(test)
#set(SRC add.cpp sub.cpp main.cpp)
#aux_source_directory(${PROJECT_SOURCE_DIR} SRC)#搜索当前路径下的.c,.cpp文件，免得挨个写
file(GLOB SRC ${PROJECT_SOURCE_DIR}/src/*.cpp)#还是搜索，但是可以对子目录递归搜索,且需要指定类型
set(EXECUTABLE_OUTPUT_PATH /home/xj/praCMAKE/v1)                                                                                                                                                                    
set(CMAKE_CXX_STANDARD 11)                       
include_directories(${PROJECT_SOURCE_DIR}/include)#有子目录时需要指定出头文件所在文件夹                                                                                                                                                                                                                                                                                                              
add_executable(app ${SRC})
