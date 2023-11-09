# Terrain_relative_navigation
Gitbook documentation [here](https://dslvaaron24.gitbook.io/terrain-relative-navigation/)
## Data generation
High resolution lunar terrain data was used as [data set](https://github.com/Rihan24/Terrain_relative_navigation/tree/main/test%20data%201) for testing  visual positioning estimation algorithm. A fule efficient three dimensional decent trajectory was generated using polynomial splines shown below.<br>
<img align="center" src="/results/Descent traj.JPG" width="40%" height="40%"/><br>
Initially we implemented a [trajectory with fixed time segments](https://github.com/Rihan24/Control_trajectory_tracking/blob/main/min_snap_trajectory_generator/fixed_time_ms.py)<br>

Then we improved it by computing [optimal time segments](https://github.com/Rihan24/Control_trajectory_tracking/blob/main/min_snap_trajectory_generator/min_snap_time_opt.py), where gradient descent is implemented to optimized time for each segment.<br>

We further modified the formulation to incorporate acceleration and velocity constraints to generate [constrained time optimized trajectory](https://github.com/Rihan24/Control_trajectory_tracking/blob/main/min_snap_trajectory_generator/constrained_time_opt.py)<br clear="right"/>
## PID based Controller
We implemented high-level position controller (lateral acceleration as control) and low level attitude controller (angular rates as control)<br>
<img src="/results/pid_tracking_1.jpeg" width="50%" height="50%"/>  <img src="/results/pid_tracking_2.jpeg" width="40%" height="40%"/><br>

## Integral Sliding Mode Controller
To mitigate the external disturbances cause by wind we implemented sliding mode control based controller<br>
<img src="/results/pid_with_disturbances.jpeg" width="40%" height="40%"/> <img src="/results/smc_with_disturbances.jpeg" width="40%" height="40%"/><br>
PID with external disturbances  vs   Sliding Mode with external disturbance

## Performance Validation on Hardware
<img src="/results/hardware_implementation.gif" width="120%" height="120%"/>
