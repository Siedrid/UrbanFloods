# Urban Floods

This repository gives multiple options to create and enhance flood delineations in urban areas. The methods are not developed by myself, but are provided by scientist from JRC and LIST. These step-by-step procedures are ment to facilitate access to the non-scientific community to these procedures. 

I developed the step-by-step guide during my work at UN-SPIDER in Bonn. The guide was originally planed to serve as a new "Recommended Practice" for flood mapping to the UN-SPIDER knowledge portal: https://www.un-spider.org/advisory-support/recommended-practices

Recommended Practices are designed to bridge the gap between the scientific and disaster management community, to facilitate access to these - in case of disaster - very usefull methods, as they are documented step by step, and require little to no knowledge of remote sensing and geo analysis. They furthermore rely only on open-access data and software.

I developed three guides, which differe in complexity. As each flood is a bit different (different because of the meteorologic circumstances, the damage done or the land cover/use class affected) the three methods differ in their sensitivity with respect to the different flood circumstances.

In the following the three methods are shortly presented. For in depth documentation, you will find slides for each practice in the respective folder in this repository.

## 1. Enhancing GFM derived Flood maps with Digital Terrain Models

This method was developed by Betterle and Salamon 2023 from JRC for improving Flood maps, that are known to have limitations in certain areas, by propagating the flood into areas where the sensor is known to have limitations in detecting water.
For optical sensors these are clouds, whereas for radar satellites these are certain land cover classes like urban fabric or dense vegetation.
This practice now uses flood delineations and exclusion masks from the Global Flood Monitoring Database. As an open-source Digital Terrain Model we recommend the FABDEM, which is a derivate of the Copernicus 30m DEM.

The practice is successfull for large floods, i. e. with an input flood raster with enough pixels classified as flood, as the propagation distance is a function of the area of the original flooded area.

## 2. Enhancing GFM derived Flood maps with DTMs and Sentinel-2 water masks
This method builds on the previous method by not only using the GFM flood delineation, but also including a Sentinel-2 flood map. As optical data has also major limitations during floodings, because of the clouds, the method uses two incomplete flood maps, merges them, and propagates the flood into the area, where both sensors are insensitive to water.
In that way, the previously mentioned method can be improved, especially if GFM under estimates the flooded area.

## 3. Flood Mapping and Damage Assessment in Urban Areas with Sentinel-1 Interferometric Coherence
Especially in dense urban areas, Sentinel-1 and Sentinel-2 imagery have challenges to detect water. Even if single flood pixels are detected inside the urban areas, also FLEXTH under estimates the area affected, as propagation distance is a function of the originally flooded area.
Also certain types of floods, like flash floods, when water does not remain inside the city, but drains quickly and leaves nothing but a lot of damage, cannot be detected with either optical or radar satellites.
This is where InSAR coherence comes in, which can be calcluated from a certain type of radar imagery.
