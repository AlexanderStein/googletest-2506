cmake_minimum_required(VERSION 3.12)
project(Test2506 CXX)
include(CTest)
find_package(GTest REQUIRED)
add_executable(Test2506 test.cpp)
target_link_libraries(Test2506 GTest::GTest GTest::Main)
gtest_discover_tests(Test2506
    EXTRA_ARGS --gtest_output=xml:${CMAKE_BINARY_DIR}/
)
