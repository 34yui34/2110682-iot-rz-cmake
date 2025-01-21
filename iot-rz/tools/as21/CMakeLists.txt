# Minimum required CMake version
cmake_minimum_required(VERSION 3.10)

# Project name
project(as21)

# Set C standard
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Add include directory
include_directories(${CMAKE_SOURCE_DIR}/include)

# Add source files to the target
add_executable(as21
    ${CMAKE_SOURCE_DIR}/src/as21.c
    ${CMAKE_SOURCE_DIR}/src/hash.c
)

target_compile_options(as21 PRIVATE -Og)

# Optionally, add compile definitions or flags
# target_compile_definitions(as21 PRIVATE <DEFINE>)

# Optionally, link to other libraries (if needed)
# target_link_libraries(as21 <other_libraries>)

