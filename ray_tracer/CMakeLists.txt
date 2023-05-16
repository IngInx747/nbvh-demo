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
target_link_libraries(${PROJECT_NAME} PRIVATE nbvh)

# stb
target_link_libraries(${PROJECT_NAME} PRIVATE stb)
