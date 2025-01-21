# Minimum required CMake version
cmake_minimum_required(VERSION 3.10)

# Project name
project(rz36-2)

# Set C standard
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Add include directory
include_directories(${CMAKE_SOURCE_DIR}/include)

# Add source files to the target
add_executable(rz36-2
    ${CMAKE_SOURCE_DIR}/src/compile.c
    ${CMAKE_SOURCE_DIR}/src/gencode.c
    ${CMAKE_SOURCE_DIR}/src/lex.c
    ${CMAKE_SOURCE_DIR}/src/list.c
    ${CMAKE_SOURCE_DIR}/src/parse.c
    ${CMAKE_SOURCE_DIR}/src/prtoken.c
    ${CMAKE_SOURCE_DIR}/src/stmt.c
    ${CMAKE_SOURCE_DIR}/src/symtab.c
    ${CMAKE_SOURCE_DIR}/src/token.c
)

target_compile_options(rz36-2 PRIVATE -Og)

# Optionally, add compile definitions or flags
# target_compile_definitions(rz36-2 PRIVATE <DEFINE>)

# Optionally, link to other libraries (if needed)
# target_link_libraries(rz36-2 <other_libraries>)

