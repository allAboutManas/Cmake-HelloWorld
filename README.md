# CMake "Hello World" Project

This project serves as a basic example for understanding how to use **CMake**, a widely-used build system generator. CMake helps streamline the build process by creating platform-specific build files that are used to compile and manage C/C++ codebases.

## Overview of CMake

CMake is a tool that simplifies the build process by generating appropriate build files for different environments (such as `Makefiles` for macOS/Linux or project files for Visual Studio on Windows). By using CMake, developers can work across multiple platforms without needing to manually adjust build configurations for each one.

### Important Concepts in CMake

- **CMakeLists.txt**: The central file in a CMake project, containing instructions for building the project. It lists source files, defines build targets, and sets other project-specific configurations.
- **Variables**: CMake allows defining variables to store settings for the project (e.g., project name, CMake version, source files).
- **Commands**: Key CMake commands include `project()` (sets the project’s name), `add_executable()` (defines an executable output), and `cmake_minimum_required()` (sets the minimum version of CMake required).

### CMake Workflow

CMake works by reading the `CMakeLists.txt` file and generating the correct build files for your platform. These files can be:
- **Makefiles** (for Unix-based systems like Linux or macOS)
- **Visual Studio or Xcode project files** (for IDEs like Visual Studio on Windows or Xcode on macOS)

Once the build files are generated, you can use your platform’s standard build tools (like `make`, `msbuild`, etc.) to compile and build the project.

## Project Structure

This project is composed of two files:

1. `hello.c` — The source code for the "Hello, World!" program.
2. `CMakeLists.txt` — The configuration file that guides the build process using CMake.

### Source Code: `hello.c`

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
