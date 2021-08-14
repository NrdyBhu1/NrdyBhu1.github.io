# [<- OpenGl](../opengl/)

## OpenGl Renderering
Opengl renders everything in vertices and triangles.  
Why triangles? - Cause triangle is the only shape with least number of side and formed with minimum vertices for a polygon.

## Understanding the Rendering
Opengl has three types of object which are involved in renderering. This is also used in something called the batch renderering.  
Batch Rendering is a technique where all of the vertices are stored prehand and and drawn all together in a single draw call. This is more efficient  
as it reduces gpu and cpu usage whereas a 1000 draws uses both the cpu and gpu drastically, hence batch rendering is more efficient.  

### VBO, VAO & IBO
**VBO**: The VBO is the vertex buffer object which contains the vertices of triangles.  
**VAO**: The VAO is the vertex attrib object which contains the position, color and differents attributes of a vertex.  
**IBO**: The IBO is the index buffer object which is responsible for the rendering of each vertex. It contains the sequence in which the vertices should be drawn.  

