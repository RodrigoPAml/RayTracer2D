# RayTracer2D

First implementation of a Ray Tracing in 2D using Box Engine with Lua and GLSL

Box engine is developed by me to create 2D and 3d applications

# Show case

![ezgif-5-3c3f808ea9](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/16672cc7-eecc-4122-853e-a39805f39d06)

![gif1](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/5c67320f-d735-4f97-9b50-5cbb4f18c266)

![ezgif-5-386e8e0582](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/a9ac4be1-9bad-4b85-b388-6e76e238fad3)

![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/85e6949d-7108-46ae-8ebc-3b619d1cf85a)

# How to use

- Click in a object to move it
- To delete a object click it and press delete
- To create a new object press space
- To scale a selected object press Q/W or A/S
- To move the light press L
- To configure resolution, number of casted rays or others, execute in the engine editor and edit 'begin_frame' or 'ray_tracer' game object

![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/f37406c1-749b-48fa-ba5d-72bdda7ed89a)

# Implementation

- Direct light is calculated by casting a ray from the pixel to the light, and cheking if no collision is detected with the rectangles.
- Indirect light is done by casting N rays (configurable) from the pixel and when it intersect with some rectangle, it checks if it reaches the light from the intersection point. From there the calculation with angle and attenuation is made and the average of light is calculated from all directions.
- Indirect light have only a single bounce.
- Take a look at the file shader.frag for mor implementation info
  
![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/4b16a707-dd52-4737-aaf1-3fed438a045d)

# Executing

- Box Engine is avaible in Engine Folders with a release and the source code is in my repository
- To run use start.sh or use start_editor.sh to use the engine editor and change settings better
- Source code of ray tracing is in Assets folder

![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/2f866ba6-1e36-4368-b2ab-bd5389c997fc)

