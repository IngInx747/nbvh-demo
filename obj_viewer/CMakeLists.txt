project(obj-viewer)

file(GLOB SRCS
    "*.h"
    "*.hh"
    "*.hpp"
    "*.c"
    "*.cc"
    "*.cpp")

add_executable(${PROJECT_NAME} ${SRCS})

# bvh
target_link_libraries(${PROJECT_NAME} nbvh)

# glm
target_link_libraries(${PROJECT_NAME} glm)

# glfw
target_link_libraries(${PROJECT_NAME} glfw)
add_dependencies(${PROJECT_NAME} glfw)

# opengl (calls opengl directly, instead of using a modern extension loader library)
find_package(OpenGL REQUIRED)
target_link_libraries(${PROJECT_NAME} OpenGL::GL)
target_link_libraries(${PROJECT_NAME} OpenGL::GLU)
