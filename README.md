# Moving_Averages_A_Custom_Designed_Clustering_Method
The following code is a quick and easy methodology to cluster (non-parametric) data points through averaging distances between points. This is an improvement over traditional randomized centroid initialization in K-means
The following code is a quick and dirty method of non-parametric clustering that seeks to cluster data based on if the cluster average is less than the total average for the dataset. 

The math behind this is very simple, an average is calculated for the entire dataset to initialize centroids. 

The distance to each point is then calculated for the initial centroids. 

The average distance to each point is then calculated. 

Next the average distance between the centroids and distance points are calculated. The mid point of this average distance becomes a new centroid. 

The distance from all the new points is then calculated to this centroid. 

If the distance is less than the initial average distance, the point joins the new centroid in a cluster. 

If the average distance for this cluster is less than the overall average distance, the cluster is kept! 

This continues until the average distance to all of the points for all of the clusters is at a minimum (less than the initial). 
