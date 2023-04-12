# Point cloud alignment with ICP
This repository contains the C++ code developed to align the transformed point cloud with the original.

## Project Objective
The objective of this project is to implement point-to-point ICP (Iterative Closest Point) using least square optimization to align the transformed point cloud with the original using PCL(Point Cloud Library).

## Dataset
The implementation is done on opensource point cloud dataset ``cloud_bin_[0-2].pcd`` and point cloud of a room ``LiDAR.pcd`` collected using Velodyne Lidar (VLP-16).

![Alt text](assets/Dataset.png)|![Alt text](assets/MappedRoom.png)
:--:|:--:
 *Opensource Point Cloud (Source: Open3D)*|*Point Cloud collected using VLP-16*

## Results
![Alt text](assets/DatasetICP.png)|![Alt text](assets/DatasetICP.gif)
:--:|:--:
 *Initial Point Clouds*|*ICP aligned Point Cloud*
 
 ![Alt text](assets/Lidar.png)|![Alt text](assets/Lidar.gif)
:--:|:--:
 *Initial Point Clouds of Room*|*ICP aligned Point Cloud of Room*

# Compiling and Running the Executable

To run the above project, clone the repository by 
```shell
git clone https://github.com/navoday01/Point-cloud-alignment-with-ICP.git
```
Now go to Point-cloud-alignment-with-ICP
```shell
cd Point-cloud-alignment-with-ICP/
```
Now create a build folder and go to it
```shell
mkdir build && cd build 
```
Run the following command to build system generator
```shell
cmake ..
```
Run the following command to drive the compiler and other build tools to build the code
```shell
make
```
Run the code by entering following in the terminal to visualize implemetation on collected Lidar point cloud. xx is the number of initial iterations to do (1 is the default value) if no value is entered.
```shell
./icp ../LiDAR.pcd xx
```
