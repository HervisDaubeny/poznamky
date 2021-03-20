Realtime algorithms

​	Based around time constraints
​		hard vs soft limits
​	Framerates
​		cinema = 24Hz, EUTV = 25(50)Hz, USTV = 30(60)Hz, Games = 30-60Hz, VR = double the Games, Haptic rendering = 1kHz
​	

Programmable Pipeline
	example being the rasterization pipeline

OpenGL
	asynchronous calls
	uses OGL objects (textures, buffers, framebuffers, shaders, ...)
	uses GL contexts which determine ownership of the OGL objects *which is needed for asynchronous work*

Rasterizer
	decomposes vector primitives into <u>fragments</u>
	**fragments** raster elements that can contribute to a colour of a pixel *meaning that we can use multiple fragments to 		represent a single pixel*
	in the **rasterization pipeline** the rasterizer works with the output of a <u>vertex shader</u>

OpenGL shading language
	a programming language allowing us to customize the rasterization pipeline
	it is used to customize the **vertex** and the **fragment shader**

History
	80s - mid 90s
	slow, limited 2D graphics
	rendering models: {wireframe, flat, flat + wireframe, lit flat, gouraud}
	SGI 1982 - geometry engine
	SGI 2 90s - reality engine

Summary
	OpenGL calls:

```OpenGL
// Shaders:
glCreateShader(), glDeleteShader(), glShaderSource(), glCompileShader(), glAttachShader(), glLinkProgram(), glProgramUniform*(), glGetUniformLocation(), ...

// Buffer objects:
glGenBuffers(), glBindBuffer(), glBufferData(), glBindVertexArray(), glGenVertexArrays(), glVertexAttribPointer(), glEnableVertexAttribArray(), glDeleteVertexArrays(), ...

// Drawing:
glDrawElements(), glDrawArrays()

// Other:
glViewPort(), glClearColor(), glClear(), glFinish()
```

