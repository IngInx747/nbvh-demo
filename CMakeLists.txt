cmake_minimum_required(VERSION 3.0)

project(NBVH-DEMO VERSION 1.0 LANGUAGES CXX)

if (${CMAKE_CURRENT_SOURCE_DIR} STREQUAL ${CMAKE_SOURCE_DIR})
    add_subdirectory(3rdparty)
    add_subdirectory(ray_tracer)
    add_subdirectory(obj_viewer)
endif()
