cmake_minimum_required(VERSION 3.7)

project(libcpl)

set(CMAKE_CXX_STANDARD 17)

include_directories(${PROJECT_SOURCE_DIR}/src/)

file(GLOB SOURCE ${PROJECT_SOURCE_DIR}/src/*.cc)

add_library(cpl STATIC ${SOURCE})

add_executable(cpl_test test/main.cc)

target_link_libraries(cpl_test cpl)