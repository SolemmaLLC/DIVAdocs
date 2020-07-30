
LEED-IEQ-8.1 Compliance
================================================
Important Update: 
	This function was updated to reflect the LEED IEQ 8.1 Addendum change to the evaluation bounds. The new LEED Illuminance bounds are 10 - 500 fc.
	
LEED Test
-------------------

Metrics >> Daylight Grid Based >> Point-in-Time Illuminance >> LEED IEQ 8.1

	This simulation tests a model for LEED NC IEQ 8.1 points. Refer to the LEED Guide for modeling information and other requirements.
	You only need to set your preference for units, respect dynamic shading and geometric modeling. The simulation will run two illuminance tests: September 21 at 9am and 3pm. The simulation tallies the percentage of the total calculation grid area that receives between 10 and 500 footcandles at each point-in-time. In order to qualify for the LEED points, a minimum of 75% of the project must be daylit at both of those times. 
	
LEED Points
--------------------
Percentage of area between  10 & 500 fc at 9am and 3pm 

- <75%: 0 points

- 75% to 90%: 1 point         

- 90% or more (schools only): 2 points

Results are displayed as follows: For a single point, if the value at 9am or 3pm is lower than 10fc, the node is categorized as "<10fc". If the value at 9am or 3pm is greater than 500fc, then node is categorized as ">500fc". If the values at 9am and 3pm both fall within the acceptable range, the results will display the average of the two.

When running the simulation, it is important to increase the ambient bounces to 5 or more. To do so, in the Radiance parameters editable field, change the item "-ab 2" to "-ab 5".

Note: 
	The DIVA LEED function gives one assessment for all of the nodes selected. It does not break the results down into node or panel groups.

 