# Argoverse2.0-Data
This is for argoverse2.0 data understanding. Motion forecasting data is being explored.

Argoverse 2.0 data understanding for Motion forecasting (250K scenarios for Training and validation, each scenarios contains 11secs long).

https://www.argoverse.org/av2.html

Argoverse2.0 data contains HD maps from US cities Austin, Detroit, Miami, Pittsburgh, Palo Alto, and Washington, D.C

Argoverse 2 Motion Forecasting Dataset: contains 250,000 scenarios with trajectory data for many object types. This dataset improves upon the Argoverse 1 Motion Forecasting Dataset.

Vector Map: Lane-level geometry: lane boundaries, lane marking types, traffic direction, crosswalks, driveable area polygons, and intersection annotations.

Lane boundaries: Dashed white, dashed yellow, double yellow Crosswalks: Purple Intersection: grey Path of ego vehicle: red

Argoverse data understanding could be used for Training vectornet for trajectory prediction.

scenarios.json file contains the information of drivable areas, lane segments with centerline, left_lane_boundary points, right_lane_boundary_points, with lane segments ID with intersection and lane type. It also includes the information of pedestrians as additional information in argoverse2.0 for training vectornet with rich information of pedestrian. 

Argoverse2.0-Map-api: 
  	1. Nearest lane segment from the query points is being found using L-infinity norm which consider the highest magnitude among each elements in the vector space i.e which considering the lane segment based on lane radius. 
	2. Nearest lane segment() function takes the query points and interpolate the query points using Interpolate_arc (Distance based interpolation along a general curve in space) and use L-infinity norm find the lane segment points which are nearest to the query points.
	3. Link for interpolation (for understanding): https://in.mathworks.com/matlabcentral/fileexchange/34874-interparc
  


