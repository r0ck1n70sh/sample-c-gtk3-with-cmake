# project
cmake_minimum_required (VERSION 3.10)
project(sample-c-gtk3-with-cmake C)


# path
set(CMAKE_SOURCE_DIR ${CMAKE_SOURCE_DIR}/src)


# dependencies
find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK3 REQUIRED gtk+-3.0)


# compile
add_executable(out ${CMAKE_SOURCE_DIR}/main.c)

target_link_libraries(out PRIVATE ${GTK3_LIBRARIES})
target_include_directories(out PRIVATE ${GTK3_INCLUDE_DIRS})

target_link_libraries(

