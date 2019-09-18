cmake_minimum_required(VERSION 2.8)
project(BST)
include(ExternalProject)

set(PROJECT_NAME BST)
set(INCLUDE_DIR include)
set(GTEST_INCLUDE_DIR /Users/ickim/dev/kata/kata_datastructure_algorithm/gtest/include)
set(SRC_DIR src)
set(TEST_DIR tests)
set(GTEST_LIB_DIR /Users/ickim/dev/kata/kata_datastructure_algorithm/gtest/lib)

set(TEST_MAIN bst_test)
set(SRC_FILE bst)

project(${PROJECT_NAME})
include_directories(${INCLUDE_DIR} ${GTEST_INCLUDE_DIR})
add_executable(${TEST_MAIN} ${TEST_DIR}/${TEST_MAIN}.cc ${SRC_DIR}/${SRC_FILE}.cc)
target_link_libraries(${TEST_MAIN} ${GTEST_LIB_DIR}/libgtest.a)

