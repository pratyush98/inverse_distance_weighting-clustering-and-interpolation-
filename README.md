# inverse_distance_weighting-clustering-and-interpolation-
its a data interpolation and prediction project using machine learning tools

challenge details: The data used for the dem-model generation is the lats, long and elevation from the mean sea level as input data we have to interpolate other 80k points and making the 3d model from scratch using elementary traingles.

methods used:

1. k-means clustering algorithm used to cluster data into small geometric groups so that data processed during interpolation uses only nearby data to interpolate not data far away from the predicted point.(only clustered points get used for interpolation)

2. For each cluster we create cloud points that are spaced according to the spacing proportional to the area of the rectangl enclosing the cluster. this gives us a uniform time of execution for each cluster.

3. For each cluster the points to be found out are weighted inversely to distance, distance*2 , e^-2*distance or e^-lamda*distance 

4. each points are then sorted according to the data latitudes and then sorted according to the longitudes data for each common latitudes. this data is entered in the delauney traingulation algorithm and it plots the traingles in 3d.

5. We create a orthographic projection of the 3d model on the screen. This is equivalent to taking the image of the 3d corners of the traingle on a oblique plane making a certain angle with the X-plane, Y-plane.
