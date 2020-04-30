cmake_minimum_required(VERSION 2.8)

include(gtest.cmake)
find_package(Threads)

project(BuildTest)


add_executable(buildtest src/main.cpp src/logic.hpp)

set (CMAKE_CXX_STANDARD 11)

add_executable(buildtest_tests gtest tests/main.cpp src/logic.hpp)
target_link_libraries(buildtest_tests gtest ${CMAKE_THREAD_LIBS_INIT})
