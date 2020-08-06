
Setting Up a Rhino Model for Daylight Analysis
==============================================

The following includes information about proper set-up of the Rhino model for use with the toolbar. To make sure that all geometry is being used in the analysis, it is a good idea to first run the “Visualization” Metric, and to examine the image for unexpected problems such as “holes” or gaps.

 

If you do not have a Rhino model available, the MIT reference model can be downloaded `here.`_
 
 .. _here.: http://web.mit.edu/sustainabledesignlab/projects/ReferenceOffice/index.html

 

Units
-----
It does not matter what units are used for the Rhino modeling: meters, millimeters, inches, feet, parsecs, etc.

 

Orientation
-----------
It is important that your project is oriented properly within Rhino with regards to North. In Rhino, as most other software, North is the top of the screen when viewing the model in a “Top” or “Plan” view such that the positive Y-axis is North.

Layers
------
DIVA does not require any specific naming conventions for layers; however, materials will be associated by layer, so you can't keep geometry with different materials on the same layer.

.. figure:: images/divalayers.jpg
   :scale: 100 %
   :align: center
   
*Layer panel showing DIVA-Created Layers*

DIVA Layers
-----------
When you run the DIVA **Location** button, several DIVA layers are created. These layers store the various nodes, node values, grid and legend information that DIVA generates.

Hidden Layers
-------------
Layers turned off will not be exported.

Locked Layers
-------------
Locked layers will not be exported.

Sublayers
---------
There are no restrictions to using sublayers.

Ground Plane
------------
A ground plane shoould always be modeled and assigned a DIVA material.

Geometry
--------
Models can be built using surfaces, polysurfaces and/or meshes, although all geometry is "invisibly" converted to temporary meshes through the DIVA process. Complicated geometry can be "pre-meshed" before running the metrics.

Thickness
---------
Glass should be modeled using single surfaces, as opposed to polysurfaces or solids.

Visibility, Locking and Hiding Layers
-------------------------------------
Only geometry on visible, unlocked layers will be exported to Radiance. Keep this in mind when running simulations.

Remember to always check that your geometry is being exported correctly by running the “Visualization” Metric and performing a visual check.




















