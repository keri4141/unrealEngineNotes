

# **Two Ways of Rendering**
<br>

  ## *Deferred Rendering (unrealEngine default) and Forward Rendering*
  **Deferred** gives stable and better performance for more demanding apps
  (weakness is antiAliasing) Temporal Anti Aliasing- causes ghosting frames


  **Forward** gives simpler and faster performance
  (limited hardware, power) MSAA in forward gives better anti alisainsg 


# **G Buffer**

Set of images for each frame, these images contain all info required for later stages of rendering process for real time compositing This happens in background. (Such as depth)

<br>

# **Pixel and Vertex Shaders** - 

  General CPU isnt good for tiny little calculations, its pretty slow

  hardware and software handle the shader calculations on the dedicatd part of the GPU


  Pixel shaders handles a bunch of the lighting, fog, rendering materials and shading



# **Frame Time** - 

  *millisec is the unit for frame creation.*<br><br>

***To measure this in the editor, type into command output log***<br>
<br>
```stat fps ``` to show frames <br>
```t.maxfps 600 ```  removes cap on frame rate<br>
```stat unit ``` will give more info<br>

<br>
<br>

# Hardware Components handle these capabillities

<table>
  <tr>
    <th>
      Game (CPU)
    </td>
    <th>
      GPU
    </th>
  </tr>
  <tr>
    <td>
    Animations
    </td>
    <td>
    lighting
    </td>
  </tr>
  <tr>
    <td>
    Physics
    </td>
    <td>
    rendering of models
    </td>
  </tr>
  <tr>
    <td>
    Collision
    </td>
    <td>
    reflections
    </td>
  </tr>
  <tr>
    <td>
    AI
    </td>
    <td>
    shaders
    </td>
  </tr>
  <tr>
    <td>
    Spawning/Destroying
    </td>
  </tr>
  <tr>
    <td>
    Scale, position, rotations
    </td>
  </tr>
</table>

<br>

# 4 Common performance issues

  ## *Intro to draw calls*
  When environment is rendered, it will render object per object, every models (mesh)
  is a draw call (for simplicity).
  <br>
  
  ## *Pixel /Vertex Impact*

  ### *Intro to Translucency rendering*
  Has to recalculate everytime a new translucent object is introduced, pixel shader operations are alot in this case
  **Shader Complexity** is a good tool to use to debug

  ### *Shadows*

  It is the dynamic shadows that are costly, not the lighting itself<br>
  Be careful with polygon count of the environment if using dynamic lighting
  Whereas static lighting, or no dynamic lighting, u can have higher polygon count





