This is a C++ OpenGL graphics project based on [these](https://learnopengl.com/Getting-started/Creating-a-window) tutorials.

In order to run this project you must have the required dependencies installed (they are mentioned in the tutorial above):
-gcc/g++
-cmake
-GLFW (library for creating windows that can run an OpenGL context)
-Glad (loader for OpenGL functions)

The following instructions are probably only relevant to Linux, so if you are using windows, please refer to the tutorial linked above.

Once you have the dependencies installed, you can generate the makefiles using cmake.
Make sure to replace "/path/to/glad" in the CMakeLists.txt to exactly where your path is. Then, run:
`cmake .`

Then, create the executable using
`make`

Sample output:
![alt text](https://github.com/glowinginthedark/openGL/raw/master/images/rectangle.png "Logo Title Text 1")

