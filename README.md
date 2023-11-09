# Terrain_relative_navigation
Gitbook documentation for theory, references present [here](https://dslvaaron24.gitbook.io/terrain-relative-navigation/) <br>
Presentation [here](https://drive.google.com/file/d/1udPQsN9tiEr7wFe63foQhQWi7pYzFkXh/view?usp=sharing)
<img src="/media/Mars-Rover-TRN.gif" width="50%" height="50%"/>  <br>
## Data generation
High resolution lunar terrain data was used as [data set](https://github.com/Rihan24/Terrain_relative_navigation/tree/main/test%20data%201) for testing  visual positioning estimation algorithm. A fule efficient three dimensional decent trajectory was generated using polynomial splines shown below.<br>
The trajectory was employed as lunar descent trajectory for simulation and testing of estimation algorithms<br> <br>
<img src="/media/ezgif.com-video-to-gif.gif" width="40%" height="40%"/> <img  src="/results/Descent traj.JPG" width="40%" height="40%"/><br>

## Fetaure matching
Features on lunar image were captured using OpenCV functionality, and matched with database satellite data.<br>
<img src="/test data 1/original data.png" width="50%" height="50%"/>  <br>
Database satellite image <br><br>
<img src="/test data 1/data_img2.png" width="50%" height="50%"/>  <img src="/test data 1/data_img4.png" width="40%" height="40%"/><br>
Instantaneous camera data from lunar lander<br> <br>
<img src="/test data 1/scan.JPG" width="50%" height="50%"/>  <img src="/test data 1/ftr_matching4.JPG" width="40%" height="40%"/><br>
Feature matching results <br>

## Camera caliberation and pose estimation
Backward propogation of detected features is used to estimate position and orientation is inertial frame <br>
<img align="center" src="/media/Capture12.jpg" width="50%" height="50%"/>  <br>

## Some results

<img align="center" src="/results/tracked traj.JPG" width="50%" height="50%"/>
