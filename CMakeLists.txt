cmake_minimum_required(VERSION 3.5.0)
project(NBVH-DEMO VERSION 1.0 LANGUAGES CXX)

string(COMPARE EQUAL "${CMAKE_CURRENT_SOURCE_DIR}" "${CMAKE_SOURCE_DIR}" NBVH_STANDALONE)

if (NBVH_STANDALONE)
    add_subdirectory(3rdparty)
    add_subdirectory(ray_tracer)
    add_subdirectory(obj_viewer)
endif()
