cmake_minimum_required(VERSION 2.8)

project (test)
set(CMAKE_BUILD_TYPE Release)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
add_library(pal SHARED src/pal.cpp)



include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
add_executable(main src/main.cpp  )
target_link_libraries(main ${CMAKE_CURRENT_SOURCE_DIR}/build/libpal.so)
