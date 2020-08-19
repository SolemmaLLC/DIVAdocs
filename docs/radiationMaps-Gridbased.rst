
Radiation Maps-Grid Based
================================================
DIVA-for-Rhino can generate climate-specific annual surface irradiation images or calculate annual irradiation at node locations. This is a powerful tool that can be used on an urban or building scale to identify locations with solar energy conversion potential or areas in need of shading due to excessive solar exposure. Comparing summer and winter period irradiation results could help optimize shading devices to maximize winter gain while minimizing summer exposure. 

.. figure:: images/MapGrid.jpg
   :width: 900px
   :align: center

*Grid-based Radiation Map Simulation Options*

Metric
---------
The cumulative sky method is described by `Robinson and Stone`_ which harnesses a Radiance module called GenCumulativeSky to create a continuous cumultaive sky radiance distribution. This cumulative sky is then used in a Radiance backwards ray-trace simulation. Compared to other approaches which use hourly calculations, this approach is significantly faster with a minimal sacrifice in accuracy.

The Daysim-based hourly method utilizes the same engine behind climate-based metrics in DIVA to produce an hourly result file in addition to the time-cumulative irradiation map. Once a radiation map has been generated using this method, different portions of the year can be visualized very quickly.

.. _Robinson and Stone: http://www.solemma.net/references/PLEA2004_RobinsonAndStone.pdf