
Scripts for Converting Geometry
================================================
We have created several scripts for converting geometry imported from other software to usable geometry in DIVA.

Revit models
-------------------
Clean Up Window Surfaces 

Updated Clean Up Window Surfaces - includes polysurfaces - Beta

This script will convert windows modeled as solids (typically from imported Revit models) to usable single surfaces. If your surfaces are imported from Revit as polysurfaces instead of meshes, use the second script. For additional information go to the Video Tutorial on working with Revit models.

TAS models
--------------
Clean Up Window Surfaces-Double Surfaces

This script will convert windows modeled as double surfaces (typically from imported TAS models) to usable single surfaces.

Sketchup models
-------------------
Organize Sketchup Geometry-Beta 

This script will organize geometry from imported \*\.dxf Sketchup models, placing the exploded geometry on the appropriate layers. This script is still in beta testing. For help or feedback, email kera@solemma.net.

Note:
	Dxf models exported from Sketchup can sometimes be too big to import into Rhino. To reduce the size, export the Sketchup model in parts if necessary, and turn of "Edges" in the Export Options dialog box.

Loading and Running Scripts in Rhino
-----------------------------------------
There are 2 basic ways to load scripts in Rhino.

- a) Drag and drop the \*\.rvb file into an open Rhino viewport window.

- b) Type LoadScript in the command line --> Click Add and browse to the \*\.rvb script that you want to load --> Highlight the script in the LoadScript box --> Click Load. To run the script in the future, type RunScript in the command line and select and run the script.