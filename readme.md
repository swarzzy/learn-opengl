# Learn OpenGL Template repository

This is a repository which contains empty Visual Studio C++ project ready for development.

Original Learn OpenGL course provides some really nasty and bad practices ragarding C++ project organization and libraries management. Here I povide ready-for-use C++ template project with all Visual studio stuff setup and a guide how to setup all libraries without scattering them all over you machine and hardcoding absolute paths.

***You can use this guide instead of Part #1 of original course.***

[Link to Learn Open GL](https://learnopengl.com/)

***You will need Visual Studio 2022***

## Steps to setup basic OpenGL environment

### **Installing GLFW <em>(library for creating window and OpenGL context)</em>**


1. Download GLFW prebuilt binaries for x64 ([GLFW Binaries](https://www.glfw.org/download.html))

2. Create `vendors/glfw` directory in the project

3. Extract `include`, `lib-vc2022` and `lisence.md` to `vendors/glfw`

4. Add GLFW to additional include directories in project settings

The path sould be `$(SolutionDir)vendors\glfw\include`

![](docs/images/1.png)

5. Add GLFW library to the list of project libraries.

Path: `$(SolutionDir)vendors\glfw\lib-vc2022\glfw3.lib`

![](docs/images/2.png)

6. Include GLFW to your Main.cpp
```
#include <glfw/glfw3.h>

int main()
{
}
```
7. Build the project. It should compile successfully.

<br><br>
### **Installing GLFW <em>(library for creating window and OpenGL context)</em>**
<br>

1. Go to [[Link](https://glad.dav1d.de/)] and generate library sources. Set all parameters as on screenshot and press generate

![](docs/images/3.png)

2. Download zip

3. Extract `src` and `include` to `vendors/glad`

![](docs/images/4.png)

4. Add GLAD to project include directories.


Path `$(SolutionDir)vendors\glad\include`

![](docs/images/5.png)

5. Add GLAD sources to your project.

Add `vendors/glad/src/glad.c`

![](docs/images/6.png)

6. Include GLAD **BEFORE** GLFW in your Main.cpp
```
#include <glad/glad.h>
#include <glfw/glfw3.h>

int main()
{
}
```
7. Build project. All should be OK. You are ready for doing OpenGL stuff now!
