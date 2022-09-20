cmake_minimum_required (VERSION 3.20)

project (cmake_example)

find_library(VI_CONNECTOR_LIB mylib1 /home/fixcdr2-lab/test2/externals/)
find_path (VI_CONNECTOR_LIB_INCLUDES square.h "${CMAKE_CURRENT_SOURCE_DIR}/externals")

add_executable (main  main.cpp)

target_link_libraries (main ${VI_CONNECTOR_LIB})
target_include_directories(main PUBLIC ${VI_CONNECTOR_LIB_INCLUDES})
