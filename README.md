![logo](http://i.imgur.com/lVMTcfS.png)


YABEE
=====
Renewed Egg exporter for the Blender 2.8

Exporting:
- Meshes
- UV layers
- Materials and textures (Initial PBR) via EEVEE/Cycles
- Armature (skeleton) animation
- ShapeKeys (morph) animation
- Non cyclic NURBS Curves

Missing features/TODO
=====
- Texture baking via Cycles
- Vertex colors

Materials & Textures: Principled Shader Support
=====
With the addition of the the principled shader in Blender and the upcomming support for physically based materials in Panda3D it was possible to extend YABEE to improve the workflow for artists when working in a PBR environment. 
Since Panda3D does not yet fully support all features offered by Blender Node System, a special Nodegroup was crafted to give easy access to the already supproted features.

The group was given the special name Panda3D_PBR (former Panda3D_RP_Diffuse_mat), this is important as YABEE will try to find this name inside the material nodes and gather its inputs. Correct names of the group input are important too (red arrows).
Group and usage as shown below:

<img src="http://pasteall.org/pic/show.php?id=8e31dccfbd796ed63a8c7d0d63e231f3" />

<img src="http://pasteall.org/pic/show.php?id=67cf5e0998de108735e6f1e9f8d458de" />

To use it, you have to switch blenders renderer to cycles, create a material for your mesh, set up the „Panda3D_PBR NodeGroup“ and connect the inputs you need as shown in the pictures. Select your model and export with YABEE. There is no need to manually select the PBR-Option. If the material uses Nodes and the nodegroup is present  YABEE will automatically export in PBR mode.
Be sure to connect all the required texture inputs, each with a UV-Map input.

If you do not have the required texture for the input, use the Empty*.png image delivered with YABEE.

The PBR node support is still work in progress, if you find important features missing please contact the developers.
