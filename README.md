# RayTracer2D

First implementation of a Ray Tracing in 2D using Box Engine with Lua and GLSL

Box engine is developed by me to create 2D and 3d applications

![ezgif-5-3c3f808ea9](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/16672cc7-eecc-4122-853e-a39805f39d06)

# How to use

- Click in an object to move it
- To delete an object click it and press delete
- To create a new object press space
- To scale a selected object press Q/W or A/S
- To move the light press L
- To configure resolution, number of casted rays or others, execute the engine editor and edit 'begin_frame' or 'ray_tracer' game object

![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/f37406c1-749b-48fa-ba5d-72bdda7ed89a)

# Implementation

- Direct light is calculated by casting a ray from the pixel to the light, and checking if no collisions are detected with the rectangles.
- Indirect light is done by casting N rays (configurable) from the pixel and when it intersect with some rectangle, it checks if it reaches the light from the intersection point. From there the calculation with angle (dot product) and attenuation is made and the average of light is calculated from all directions.
- Indirect light have only a single bounce.
- Take a look at the file shader.frag for mor implementation info

# Show case

![ezgif-5-386e8e0582](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/a9ac4be1-9bad-4b85-b388-6e76e238fad3)

![gif1](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/5c67320f-d735-4f97-9b50-5cbb4f18c266)

![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/85e6949d-7108-46ae-8ebc-3b619d1cf85a)

## Light interaction

- This image describes how light interact in the real world (direct vs indirect), note that in the shader, the calculations starts from the pixels being draw and not from the actual light
    
![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/4b16a707-dd52-4737-aaf1-3fed438a045d)

# Executing

- Box Engine is available in Engine Folders with a release and the source code is in my repository (note that versions might differ)
- To run use ```start.bat``` or use ```start_editor.bat``` to use the engine editor and change settings better
- The complete source code of the ray tracing is in Assets folder

![image](https://github.com/RodrigoPAml/RayTracer2D/assets/41243039/2f866ba6-1e36-4368-b2ab-bd5389c997fc)

