# CMakeLists of libraries to build as static libs.
# The libs are used by multiple executables and other libs.

# glfw
set(GLFW_BUILD_DOCS "Build the GLFW documentation" OFF)
set(GLFW_INSTALL "Generate installation target" OFF)
add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/glfw")

# bvh
add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/nbvh")

# glm
add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/glm")

# stb
add_library(stb INTERFACE)
target_include_directories(stb INTERFACE "${CMAKE_CURRENT_LIST_DIR}/stb")
