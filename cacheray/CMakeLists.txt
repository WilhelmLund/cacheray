cmake_minimum_required(VERSION 3.5)

project(cacheray)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

set(CMAKE_C_STANDARD 11)

add_library(cacheray STATIC
        src/cacheray.c
        src/cacheray-utils.c )

target_include_directories(cacheray
        PUBLIC
        ${PROJECT_SOURCE_DIR}/include)

add_subdirectory(test)
add_subdirectory(tracecheck)

