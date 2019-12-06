![logo](http://i.imgur.com/lVMTcfS.png)


YABEE 14.1
=====
Renewed Egg exporter for the Blender 2.8 and Panda3D

Exporting:
- Meshes
- UV layers
- Textures (Initial PBR) via EEVEE/Cycles
- Armature (skeleton) animation
- ShapeKeys (morph) animation
- Non cyclic NURBS Curves

Missing features/TODO
=====
- Materials & Vertex colors
- Texture baking via Cycles

Principled Shader Support
=====
With the addition of the the Principled BSDF shader in Blender and the upcomming support for physically based materials 
in Panda3D it was possible to extend YABEE to improve the workflow for artists when working in a PBR environment. 

<img src="http://pasteall.org/pic/show.php?id=c278bebee6e22ce886ffd4448948c70f" />
<p style="font-size: small">Cube in Panda3D via pview</p>

<img src="http://pasteall.org/pic/show.php?id=0ba65151691c7eb6873771d89c77c466" />
<p style="font-size: small">YABEE becomes more Blender-compatible: No special Nodegroup is needed anymore</p>

To use it, you have to create a material for your mesh, set up the Principled BSDF shader 
by connecting at least the Image Texture shader and optionally UV Map.

The PBR node support is still work in progress, if you find important features missing please contact the developers.

**Use this version of YABEE carefully. It may contain bugs and may not work for objects with complex node system 
applied**
