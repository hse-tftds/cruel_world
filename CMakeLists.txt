cmake_minimum_required(VERSION 3.25)
project(cruel_world VERSION 0.1)

include(cmake/CPM.cmake)

CPMAddPackage("gh:NVIDIA/stdexec#nvhpc-23.09-rc2")
CPMAddPackage("gh:fmtlib/fmt#10.1.1")

add_subdirectory(src)
