# Minimum required CMake version
cmake_minimum_required(VERSION 3.10)

# Project name
project(sim21)

# Set C standard
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Add include directory
include_directories(${CMAKE_SOURCE_DIR}/include)

# Add source files to the target
add_executable(sim21
    ${CMAKE_SOURCE_DIR}/src/io.c
    ${CMAKE_SOURCE_DIR}/src/load.c
    ${CMAKE_SOURCE_DIR}/src/mon.c
    ${CMAKE_SOURCE_DIR}/src/s21.c
)

target_compile_options(sim21 PRIVATE -Og)

# Optionally, add compile definitions or flags
# target_compile_definitions(sim21 PRIVATE <DEFINE>)

# Optionally, link to other libraries (if needed)
target_link_libraries(sim21 PRIVATE m)

