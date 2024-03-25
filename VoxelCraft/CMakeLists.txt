# CMakeList.txt : CMake project for VoxelCraft, include source and define
# project specific logic here.
#

include_directories(${CMAKE_SOURCE_DIR}/lua_files)
#include <lua_files/lua.hpp>         // Include Lua headers first
#include <LuaBridge/LuaBridge.h> // Then include LuaBridge headers


# Add source to this project's executable.
add_executable (VoxelCraft "VoxelCraft.cpp" "VoxelCraft.h")

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET VoxelCraft PROPERTY CXX_STANDARD 20)
endif()

target_compile_features(VoxelCraft PUBLIC cxx_std_20)

# TODO: Add tests and install targets if needed.
