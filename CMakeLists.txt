cmake_minimum_required(VERSION 3.13 FATAL_ERROR)
project(optix_cuda_experiments LANGUAGES CXX CUDA)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(CMAKE_MODULE_PATH
    "${CMAKE_SOURCE_DIR}/CMake"
    ${CMAKE_MODULE_PATH}
)

# Locate the NVRT distribution.  Search the SDK first, then look in the system.
set(OptiX_INSTALL_DIR "" CACHE PATH "Path to OptiX installed location.")

# add_subdirectory(cuda_cmake_example)
# add_subdirectory(cuda_cmake_ptx_example)

add_subdirectory(optixHello)

source_group("CUDA Files" REGULAR_EXPRESSION ".+\\.cu$")