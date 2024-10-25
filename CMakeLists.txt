cmake_minimum_required(VERSION 3.12..3.29)

project(tiny-aes VERSION 1.0.1)

option(TINY_AES_TESTS "Configure test cases" ${PROJECT_IS_TOP_LEVEL})
option(TINY_AES_INSTALL "Configure install target" ON)

add_subdirectory(src)

if (TINY_AES_TESTS)
  include(CTest)
  add_subdirectory(tests EXCLUDE_FROM_ALL)
endif ()

if (TINY_AES_INSTALL)
  include(cmake/install.cmake)
endif ()
