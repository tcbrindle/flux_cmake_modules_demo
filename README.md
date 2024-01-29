
# Flux CMake starter project #

This is a small CMake project to demonstrate the use of the [Flux library](https://github.com/tcbrindle/flux) with C++20 modules.

It uses CMake's [`FetchContent`](https://cmake.org/cmake/help/latest/module/FetchContent.html) to automatically download the latest revision of Flux from the main branch on Github.

> Note that C++20 modules support in compilers, build systems and the Flux library itself is very new, and you may run into bugs as a result. If you'd rather use "traditional" header files instead, you can find an equivalent starter project in [this repository](https://github.com/tcbrindle/flux_cmake_demo).

## Requirements ##

* CMake v3.28 or later, using the Ninja or Visual Studio 2022 generators
* Ninja v1.11 or later (if using the Ninja generator)
* Clang 16 or later

As of January 2024, Visual Studio 17.8 can compile the Flux module, but any non-trivial usage is very likely to run into compiler bugs. It's strongly recommended to stick to using Flux via header files with MSVC for now.

GCC 13 and below are not supported by CMake for building C++20 modules. The latest development version (which will become GCC 14) is reported to work, but has not been tested with this project.
