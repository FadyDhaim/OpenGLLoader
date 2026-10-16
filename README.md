# OpenGLLoader
CMake static library target built around Pre-Generated GLAD for OpenGL 4.6 Core Profile for C/C++.

## Use Via CMake FetchContent
```cmake
cmake_minimum_required(VERSION 4.3)
project(<Your OpenGL Project>)

add_executable(<Your OpenGL Executable Target Name>)

include(FetchContent)

FetchContent_Declare(
        OpenGLLoader
        GIT_REPOSITORY https://github.com/FadyDhaim/OpenGLLoader.git
        GIT_TAG main
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(OpenGLLoader)

target_link_libraries(<Your OpenGL Executable Target Name> PRIVATE OpenGLLoader)
```
*note that your target doesn't have to be executable; for example, it may be a static library.*
