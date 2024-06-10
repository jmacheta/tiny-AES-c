cmake_minimum_required(VERSION 3.12..3.29)

project(tiny-aes VERSION 1.0.0)

option(TINY_AES_TESTS "Configure test cases" OFF)

add_subdirectory(src)

if (TINY_AES_TESTS OR PROJECT_IS_TOP_LEVEL)
  enable_testing()
  add_subdirectory(tests EXCLUDE_FROM_ALL)
endif ()
