add_library(tiny-aes aes.c)

target_include_directories(
  tiny-aes PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_LIST_DIR}/include>
                  $<INSTALL_INTERFACE:include>)
