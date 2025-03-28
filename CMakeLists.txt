cmake_minimum_required(VERSION 3.29.0)
project($(PROJECT_NAME)
    VERSION 0.0.1
    DESCRIPTION "a demo for cmake c tsk building"
    HOMEPAGE_URL "https://github.com/ljz2019gh/cmake_demo_prj"
    LANGUAGES C ASM
    )    

#全局变量设置
set(CMAKE_C_STANDARD 99)
set(CMAKE_VERBOSE_MAKEFILE ON CACHE BOOL "ON" FORCE)  # Gives more info on what cmake is doing
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../debug) # directory where ouput is generated       

#设置包含头文件路径变量
set(cpu_dir ${CMAKE_SOURCE_DIR}/src/cpu)
set(cstart_dir ${CMAKE_SOURCE_DIR}/src/cstart)
set(itest_dir ${CMAKE_SOURCE_DIR}/src/itest)
set(main_dir ${CMAKE_SOURCE_DIR}/src)
#目录添加到所有目标（targets）的包含目录列表中
include_directories(${cpu_dir} ${cstart_dir} ${itest_dir} ${main_dir})

#添加子目录
add_subdirectory(src)


