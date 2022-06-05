# 3D-Projective-Geometry-I
###### The objective is to add the color index in a 2D image, this color index indicates the depth of each point in this image. We will use transformations provided by a dataset to project a 3D point cloud on the image plane of a color camera (the camera takes the image, then the lidar create a 3D point cloud). This allows to know the depth of a set of 2d points in the image. The color of each point indicates the depth of that point.

###### Preliminary step : 
- We are interested in the RAW section of the dataset from the following link: http://www.cvlibs.net/datasets/kitti/. 
- We have installed pykitti on our python distribution.

###### List of steps to perform :
1.   Import the dataset, then read an image from the camera (camera 2) and the matrix of 3D lidar points
2.   Remove the lidar points that may be behind the camera (that are less than a 5 meter threshold in the x-axis (for lidar, the direction of the x-axis is a forward direction)), i.e., eliminate the lidar points that are behind the 180° view area of the camera. 
3.   Lidar to camera transformation 
4.   Projection into the camera image
5.   Filtering of the projection points that have coordinates outside the range of the image size, then displaying 
6.   Colorization of the points using the third z-coordinate of the lidar matrix

Lidar transformation and projection on a camera (3D to 2D):
We will use the RAW section of the dataset, the date sequence = "2011_09_26" and drive = "0009".
