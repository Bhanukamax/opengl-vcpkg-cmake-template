# Basic template for working with OpenGL in c++

## Features
- uses [vcpkg](https://github.com/microsoft/vcpkg) for package management
- [cmake](https://cmake.org/) for build system
- No special IDE needed

## Prerequisite
- Install vcpkg
- Install cmake

## How to use
- edit `CMakeLists.txt` and edit the following line to have the path to your vcpkg
```cmake
   set(CMAKE_TOOLCHAIN_FILE "{path_to_vcpkg}/scripts/buildsystems/vcpkg.cmake")
```
- create a folder called `build`
- cd into build
- run `cmake ..` to generate build files
- to build the project run `make` from the build directory
