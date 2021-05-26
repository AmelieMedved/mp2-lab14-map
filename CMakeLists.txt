cmake_minimum_required(VERSION 2.8)

set(CMAKE_CXX_STANDARD 11)
set(PROJECT_NAME mp2-lab14-map)
project(${PROJECT_NAME})

set(SortMapLib SortMapLib)
set(IteratorLib IteratorLib)
set(MapLib MapLib)
set(main main)

set(MP2_LIBRARY "${PROJECT_NAME}")
set(MP2_TESTS   "test_${PROJECT_NAME}")

set(CMAKE_CONFIGURATION_TYPES "Debug;Release" CACHE STRING "Configs" FORCE)
if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE Release)
endif()

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/MapLib) 
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/SortMapLib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/IteratorLib)

add_subdirectory(MapLib)
add_subdirectory(main)
add_subdirectory(gtest)
add_subdirectory(test)
add_subdirectory(SortMapLib)
add_subdirectory(IteratorLib)