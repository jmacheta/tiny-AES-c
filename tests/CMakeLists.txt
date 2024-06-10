add_executable(tiny-aes_ut test.c)
target_link_libraries(tiny-aes_ut PRIVATE tiny-aes)

add_test(NAME tiny-aes_ut COMMAND $<TARGET_FILE:tiny-aes_ut>)