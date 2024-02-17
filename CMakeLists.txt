cmake_minimum_required(VERSION 3.27)
project(HM_Projects C)

set(CMAKE_C_STANDARD 11)


include_directories("C://OpenSSL-Win64//include")

link_directories("C://OpenSSL-Win64//lib")

add_executable(HM_Projects
        test.c)

add_executable(test test.c)

target_link_libraries(test libcrypto.lib;libssl.lib)
target_link_libraries(HM_Projects libcrypto.lib;libssl.lib)
