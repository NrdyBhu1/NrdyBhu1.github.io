---
layout: post
title: "OpenGl Basics"
author: "NrdyBhu1"
tags: Tutorial Opengl
excerpt_separator: <!--more-->
---

This is written for version opengl 3.3. Basic modules required are GLFW and glad.<!--more-->

## Windowing
**Note:** glfw functions cannot be called with calling `glfwInit`
Create a window and set it to be current
```C
GLFWwindow* window = glfwCreateWindow(width, height, title, NULL, NULL);
glfwMakeContextCurrent(window);
```

## Loading gl functions
**Note:** gl functions should only be loaded after creating a window
Load glad and set it's view port
```C
gladLoadGL();
glViewport(0, 0, width, height);
```

## Main loop
```C
while (!glfwWindowShouldClose(window)) {
    // Code
    glfwPollEvents();
}
```

## Rendering
```C
// Loop Start
glClearColor(r, g, b, a);
glClear(GL_COLOR_BUFFER_BIT);
// Loop End
```
Here each of rgba must be between `0.0f` and `0.01f`.

## Positioning
Opengl places (0, 0) coordinates in the middle of the screen. Therefore the leftside is (-1, 0), the rightside is (1, 0), the top is (0, -1) and the bottom is (0, 1).

