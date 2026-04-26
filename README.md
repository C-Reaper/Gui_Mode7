## Project README

### Overview
This project is a simple Mode 7 graphics emulator implemented in C. The emulator allows for basic 3D to 2D projection, enabling users to visualize 3D objects in a 2D plane.

### Features
- Basic Mode 7 graphics projection.
- User controls for movement and rotation of the 3D scene.
- Support for loading textures from image files.

### Project Structure

#### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects: X11 for Linux, WinAPI for Windows, WINE for cross-compiling to Windows

## Build & Run

### Build Process
To build the project, navigate to the project directory and run the appropriate makefile based on your operating system:

```sh
# For Linux
cd <Project>
make -f Makefile.linux all

# For Windows
make -f Makefile.windows all

# For Linux cross-compile for Windows (WINE)
make -f Makefile.wine all

# For WebAssembly using Emscripten
make -f Makefile.web all
```

### Execution
After building the project, you can run it by executing:

```sh
# For Linux and Wine output
make -f Makefile.(os) exe

# For Windows output (run in WINE environment)
WINEPREFIX=~/wine64 WINEARCH=win64 wine build/Main.exe
```

### Clean Build
To clean the build directory and remove all generated files:

```sh
# For Linux
make -f Makefile.linux clean

# For Windows
make -f Makefile.windows clean

# For Linux cross-compile for Windows (WINE)
make -f Makefile.wine clean

# For WebAssembly using Emscripten
make -f Makefile.web clean
```