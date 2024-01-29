
cmake_minimum_required(VERSION 3.28)

project(flux-modules-demo CXX)

include(FetchContent)

FetchContent_Declare(
    flux
    GIT_REPOSITORY https://github.com/tcbrindle/flux.git
    GIT_TAG main # Replace with a git commit id to fix a particular revision
)

set(FLUX_BUILD_MODULE On)

FetchContent_MakeAvailable(flux)

add_executable(demo demo.cpp)
target_link_libraries(demo PUBLIC flux::module)
set_target_properties(demo PROPERTIES CXX_EXTENSIONS Off)
