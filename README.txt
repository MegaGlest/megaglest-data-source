
                                  MEGAGLEST

                     by Titus Tscharntke and Mark Vejvoda

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
                              MegaGlest Data Source README
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For tutorials and videos relating to how to work in blender and Glest see:
http://glest.wikia.com/wiki/Blender

==================================================
Using Blender 2.4x - 2.6x to export models to G3D format:
==================================================

1. Install Megaglest or Acquire the blender python plugin

2. Install a version of Blender (2.4x - 2.6x)

3. Run blender, then on the top left-hand corner click on "file". In the list 
   that pops up select "user preferences". In Tab "Addons" Now go to categories 
   and pick "Import-Export". Click "Install Add-on". Now navigate to your 
   "MegaGlest/blender" folder (or where-ever you have the blender python plugin 
   located), and pick the file called:
   Blender < 2.5x: g3d_support.py
   or Blender < 2.6x: g3d_support_b257.py
   or Blender = 2.6x: g3d_support_b260.py

   and click "install add-on".

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


Model Positioning:
==================
The X axe is the floor and the Y axe is the elevation.  The center
of the Blender's 3D space will be the center of you object, at the
ground level.  


(Non) Animating Models:
=======================
The g3d format only knows Animations! If you have a non animating model, 
you first have to set the start frame and the end frame to '1' in blenders 
'timeline'-window. Otherwise a non animating animation will be exported, 
containing a lot of frames and your model gets really big.


Exporting:
==========
Select all objects you want to export in Object mode. Then export 
to g3d via File->Export->"Glest 3d File(.g3d)".
Hint: Before doing any texturing or animation, try to export your model and
check your python console (the terminal which opens Blender) to see
if there is a warning/problem.


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

Material Transparency:
----------------------
To make a Material transparent you can toggle on z-transparency on the material 
buttons window. The degree of transparency can be set with the alpha slider 
to the right. ( This effect also allows transparent teamcolors! More about 
teamcolors and transparency from textures aplha channel below )


Teamcolor/Texture-Transparency:
===============================
Teamcolor is a special area in models, such as a building's flag or a warrior's 
shield where the color is that players's unique player color. This is the color 
that appears on the minimap as well as is used to ensure units of different 
players can be recognized as so. When creating mods, all units should have 
teamcolor at least somewhere, and it should be noticeable to ensure that players 
can distinguish their units from an ally's or enemies units. 
The teamcolor in MegaGlest is the alpha-channel (transparency) of the textures.

Toggling between transparency and teamcolor:
--------------------------------------------
 Toggling between the object having transparency or teamcolor is done by 
 selecting single sided or double sided rendering in blender. (Every model in 
 MegaGlest is doublesided so nothing is lost)

   1. In object mode select your mesh.
   2. In the Buttons Window, switch to the Editing screen (F9)
   3. Under Mesh, switch between 
         double-sided (teamcolor) and single-sided (transparency) 

Activating teamcolor/Transparency:
----------------------------------
 In the model's texture, transparency will be replaced as teamcolor. 
 To use it, you need to a texture in a format which supports transparency, 
 (either TGA or PNG).


Animation:
==========
You can export all animations made with blender. ( everything made with the 
armature system works for sure )
To do so have to set the start frame and the end frame in the 'timeline'-window
to define the animation length which will be exported. then go to object mode as 
usual and export. ( Animated models cannot be imported to blender! In old 
blender/exporter versions it was possible to import at least as shaped keys, 
but this is no longer possible. So the model is theer but the Animation is lost ) 

Number of Vertices:
===================
There is no limit for vertices in the engine itself, but typical units have 
250-1000 vertices where 1000 is already a really big model.



