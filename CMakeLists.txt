cmake_minimum_required(VERSION 3.5)
project(Diamond)

add_subdirectory(external/googletest)
include_directories(external/googletest/googletest/include)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++14")

set(SOURCE_FILES source/DiamondTestSuite.cpp source/Diamond.cpp source/Diamond.hpp)
add_executable(Diamond ${SOURCE_FILES})
target_link_libraries(Diamond gtest gtest_main)
