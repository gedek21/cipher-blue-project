cmake_minimum_required(VERSION 3.10)
project(cipher-blue-project LANGUAGES C VERSION 1.0)

# Set C standard
set(CMAKE_C_STANDARD 11)

# Add library
add_library(utils STATIC src/utils.c)
target_include_directories(utils PUBLIC ${CMAKE_SOURCE_DIR}/include)

# Add executable
add_executable(cipher-blue-project src/main.c)
target_link_libraries(cipher-blue-project PRIVATE utils)