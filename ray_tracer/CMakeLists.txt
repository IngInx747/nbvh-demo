project(ray-tracer)

file(GLOB SRCS
    "*.h"
    "*.hh"
    "*.hpp"
    "*.c"
    "*.cc"
    "*.cpp")

add_executable(${PROJECT_NAME} ${SRCS})

# bvh
target_include_directories(${PROJECT_NAME} PRIVATE "${BVH_INCLUDE_DIRS}")

# stb
target_include_directories(${PROJECT_NAME} PRIVATE "${STB_INCLUDE_DIRS}")
