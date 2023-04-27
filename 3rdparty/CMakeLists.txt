# CMakeLists of libraries to build as static libs.
# The libs are used by multiple executables and other libs.

# glfw
set(GLFW_BUILD_DOCS "Build the GLFW documentation" OFF)
set(GLFW_INSTALL "Generate installation target" OFF)
add_subdirectory("${CMAKE_CURRENT_LIST_DIR}/glfw")

# bvh
set(BVH_INCLUDE_DIRS "${CMAKE_CURRENT_LIST_DIR}/nbvh" CACHE INTERNAL "bvh include path")

# glm
set(GLM_INCLUDE_DIRS "${CMAKE_CURRENT_LIST_DIR}/glm/glm" CACHE INTERNAL "glm include path")

# glfw
set(GLFW_INCLUDE_DIRS "${CMAKE_CURRENT_LIST_DIR}/glfw/include" CACHE INTERNAL "glfw include path")

# stb
set(STB_INCLUDE_DIRS "${CMAKE_CURRENT_LIST_DIR}/stb" CACHE INTERNAL "stb include path")
