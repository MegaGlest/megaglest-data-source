
                                  MEGAGLEST

                     by Titus Tscharntke and Mark Vejvoda

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
                              MegaGlest Data Source README
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

==================================================
Using Blender 3.61 to export models to G3D format:
==================================================

1. Install Megaglest or Acquire the blender python plugin

2. Install Blender 2.61

3. Run blender, then on the top left-hand corner click on "file". In the list 
   that pops up select "user preferences". Now go to categories and pick 
   "Import-Export". Click "Install Add-on". Now navigate to your 
   "MegaGlest/blender" folder (or where-ever you have the blender python plugin 
   located), and pick the file called "g3d_support.py" and click 
   "install add-on".

4. Now the G3D importer/exporter should show up on your import/export list, 
   in the user preferences addons view. The Plugin will be called 
   "Import-Export:G3D Mesh Import/Export". Enable the check-box by clicking on 
   the right hand side checkbox.

5. Then close the window by clicking the X.

6. Now you are ready to import / export. (from the file menu select Import or
   Export and the G3d File option should be displayed).

==================================================
Model preparation and some hints to export to G3D:
==================================================

Texture/Material:
=================
Textures are the 2D images placed on 3D models to give them their surface looks. 
For example, a simple cube model could be turned into a wooden box, or a man 
could have clothing designed for him. To apply the texture, the modeller must 
link the texture to the model.

Linking the texture:
--------------------
   1. Go to the shading screen of the buttons window.
   2. Head to the material buttons subscreen.
   3. Add a new link to the object.
   4. Head to the texture buttons subscreen.
   5. Add a new texture
   6. Set the type to image.
   7. Load the image. 


