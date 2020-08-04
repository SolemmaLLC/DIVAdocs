
Custom Radiance Materials
==============================

By default, DIVA instantiates each project with the default materials file, located in **C:\\\DIVA\\\Daylight\\\material.rad.** Project-specific materials can be defined in the **.\\\ProjectName - DIVA\\\Resources\\\material.rad** file. The ProjectName - DIVA directory is located in the same folder as your Rhino file. When the materials button is clicked, materials are always loaded from the project-specific material.rad file. The project-specific file can be overwritten with the default file by running the **Location** command.

 

Any Radiance material primitive can be defined in these files and selected for use in daylighting simulations. 

There are several websites which document possible Radiance materials,

- `LBL's Radiance Materials Page`_
- `Radiance Materials Notes at Artifice`_
- `Design Integration Laboratory's Basic Radiance Materials Library`_
- `BPS Wiki's Radiance Material Database`_

.. _LBL's Radiance Materials Page: https://floyd.lbl.gov/radiance/refer/ray.html

.. _Radiance Materials Notes at Artifice: http://www.artifice.com/radiance/rad_materials.html

.. _Design Integration Laboratory's Basic Radiance Materials Library: https://web.archive.org/web/20170210051913/http://www.designlaboratory.com/computing/tools/radiance/radmatlib.html

.. _BPS Wiki's Radiance Material Database: https://web.archive.org/web/20160411161336/http://archbps1.campus.tue.nl/bpswiki/index.php/Radiance

A Note of Caution
------------------
If a Radiance material primitive is incorrectly defined, the Radiance program oconv will fail, causing all DIVA simulations to fail. If your simulations suddenly do not work after adding a new material, check that it is defined appropriately in material.rad and re-run the **Materials** command.

Defining a Custom Metal Material
-----------------------------------
For example, to add a custom reflective metal material into DIVA, we can see from `Radiance Materials Notes at Artifice`_ that the 'Metal' primitive is defined as below, where specularity is typically greater than 0.9 and roughness is typically in a range from 0-0.2.

.. _Radiance Materials Notes at Artifice: http://www.artifice.com/radiance/rad_materials.html

``modifier metal material_name``

``0``

``0``

``5 red_reflectance green_reflectance blue_reflectance sp``

Thus, the following lines can be added to the C:\DIVA\Daylight\material.rad file to define a metal material type for use in simulations,

``void metal SimpleMetal_0.44``

``0``

``0``

``5 0.44 0.44 0.44 0.9 0.125``

Defining a Custom Glass Material
-----------------------------------
For glass definitions, Radiance requires that the user translates transmission (Tn) to transmissivity (tn).

For instance if you wanted to define a glass material with a 65% transmission, the definition would be:

``void glass Glass_Transmission_65``

``0``

``0``

``3 0.7085 0.7085 0.7085``

Above, the R, G, and B transmissivity factors are derived from the transmission of the glass. For more information, see: http://radsite.lbl.gov/radiance/refer/ray.html#Materials.

For an easy way to convert transmission to transmissivity, you can use the Excel converter below. 

 

Download the Excel Transmissivity Converter here.







