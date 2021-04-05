cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

# This is a typical pattern used by projects, to prevent
# their tests being built and run, if they are
# loaded as a sub-project
if(NOT DEFINED PROJECT_NAME)
    set(NOT_SUBPROJECT ON)
else()
    # turn NOT_SUBPROJECT off, in case it was already turned
    # on in a parent scope:
    set(NOT_SUBPROJECT OFF)
endif()

project(demo-cmake-subproject-error LANGUAGES CXX VERSION 0.0.1)

if(NOT_SUBPROJECT)
    add_subdirectory(dependencies)
    add_subdirectory(tests)
endif()
