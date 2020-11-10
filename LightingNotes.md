# Lighting Basics
## LightMaps
Lightmaps is a texture that is applied to a model.<br>

## Baked Lighting - Light Mass

Lightmass is a built in software within unreal that preCalculates and the light calculations of *stationary & static* lights.

<br>

*Moveable* lights do not have dynamic indirect light bounces without a dynamic global illumination method. None of the light they cast gets baked into light maps, and do not need light maps.

<br>



# Lighting Effects & Reflections
## IES Textures & Caustics
<b>Located in Light Profiles</b><br>
Helps change the light's intensity and shape across the surface.<br>
IES textures are used to help enrich lighting on all types of lighting.<br>
Light functions can be used to create the light ripple effects on watter ( water caustics)<br>
Change Material Domain to Light function, and have output of texture to be emissive color, be sure to set light to be moveable. (No shadows for performance)<br>
## Fog & Volumetric Light

### Atmospheric Fog
There is a property in the directional light (Advanced) - Atmosphere / Fog sunLight, which adjusts the color of the angle and position of the directional light

### Exponential Height Fog
Directional InScattering color is the color of the sun<br>
Fog HeightFallOff - Fog reduces in opacity the higher you go<br>
<b>On Directional Light </b><br>
light Shaft occlusion gives you dark rays<br>
bloom gives you bright rays<br>

### Volumetric Fog
<b>Exponential Height Actor must be active</b><br>
Within Exponential Height Actor there is a property within it to activate Volumetric Fog


