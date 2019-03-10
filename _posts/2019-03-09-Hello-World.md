---
layout: post
title: Advanced Ray Tracing Part 1
---
This post will be the beginning of the post series which I will share the experience on coding a ray tracer in C++. I will share a information about my working environment and the steps that I am taking in this part of the ray tracer. In addition to these, I will share images and their rendering time. 

I am using Intel® Core™ i5-3230M and Ubuntu 18.04 as a working environment.


### Implementation
---
In this part of the ray tracer implementation, ray tracer will include core ray tracer properties such as object intersections, diffuse and specular shading, reflection and refraction (transparency) ...

Before starting the implementation of the ray tracer, I need a parser for the for transferring the values from the XML file to the scene object which have objects, light, cameras and other related variables. For this, I used TinyXML library to parse the XML file to my object. 

Since ray tracer is very suitable for OOP programming and its properties(inheritance...), I used the advantage of it while implementing my ray tracer. I constructed objects for the shapes and I also defined ray as a object for more appropiate inputs to my functions. 

While implementing the ray tracer, most of the time I encountered problem because of the mathematical mistakes that I forget. But the most tricky part in this part of the ray tracer is implementing the transparent objects in ray tracer, I have several mistakes and images differences in my implementation. I am unable to solve the problem related to the reflection in the glass object because of that the cornellbox_glass image is not quite true. In addition to that, the same problem gives differences in scienceTree as well.

While implementing my raytracer, I mainly used the our lecture notes, Fundementals of Computer Graphics , pbrt and scratchpixel introduction notes.
### Future Tasks
---
* Solving Transparency Problem
* Multisampling
* Accelaration Structures
* Distirbution Ray Tracing(Depth of Field, Glossy Reflection, Soft Shadows)

## Images
---

#### bunny.xml (512 X 512) in 23,512 seconds
![_config.yml]({{ site.baseurl }}/images/bunny.png)

----
#### spheres.xml (720 X 720) in 0.295 seconds
![_config.yml]({{ site.baseurl }}/images/spheres.png)

----
#### cornellbox.xml (800 X 800) in 0.927 seconds
![_config.yml]({{ site.baseurl }}/images/cornellbox.png)

----
#### cornellbox_glass.xml (800 X 800) in 1,702 seconds 
![_config.yml]({{ site.baseurl }}/images/cornellbox_glass.png)

----
#### scienceTree.xml (1440 X 720) in 1 minute 35,593 seconds
![_config.yml]({{ site.baseurl }}/images/scienceTree.png)
