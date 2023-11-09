# Terrain_relative_navigation
Gitbook documentation [here](https://dslvaaron24.gitbook.io/terrain-relative-navigation/)
## Data generation
High resolution lunar terrain data was used as [data set](https://github.com/Rihan24/Terrain_relative_navigation/tree/main/test%20data%201) for testing  visual positioning estimation algorithm. A fule efficient three dimensional decent trajectory was generated using polynomial splines shown below.<br>
The trajectory was employed as lunar descent trajectory for simulation and testing of estimation algorithms<br>
<img src="/media/ezgif.com-video-to-gif.gif" width="40%" height="40%"/><br>  <img  src="/results/Descent traj.JPG" width="40%" height="40%"/><br>

## Fetaure matching
Features on lunar image were captured using OpenCV functionality, and matched with database satellite data.<br>
<img src="/results/pid_tracking_1.jpeg" width="50%" height="50%"/>  <img src="/results/pid_tracking_2.jpeg" width="40%" height="40%"/><br>

## Integral Sliding Mode Controller
To mitigate the external disturbances cause by wind we implemented sliding mode control based controller<br>
<img src="/results/pid_with_disturbances.jpeg" width="40%" height="40%"/> <img src="/results/smc_with_disturbances.jpeg" width="40%" height="40%"/><br>
PID with external disturbances  vs   Sliding Mode with external disturbance

## Performance Validation on Hardware
<img src="/results/hardware_implementation.gif" width="120%" height="120%"/>
