cmake_minimum_required(VERSION 3.22.0)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

project(Leaver)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
add_library(LeaverLib SHARED leaver.h leaver.cpp)

add_executable(LeaverClient LeaverLibraryClient.cpp)
target_link_libraries(LeaverClient LeaverLib)