# Sensor Fusion using EKF
This repository include an example application of Extended Kalman Filter using  ```robot_pose_ekf``` cROS package on gazebo turtle bot simulation package using its IMU and wheel odometry data

## Directory Structure


## Steps to launch the simulation

## Output

# Kalman Filter

One way of looking at Kalman filter is to consider it as any other types of filter. Filters are designed to eliminate or reduce noise from signal. Kalman filter, similarly, tries to eliminate uncertainty and noise from the data regarding the states of a system. Kalman fiter accepts a noisy measurement from sensors and assumes that the signals have Gaussian ditribution, and therefore, they can be described by their means and variance. This assumption is the main basis for Kalman filters. It also accepts inital guess about the states of the system, and then, it uses system models (State Transition Function in State Space modelling) to predict the next values for states of the system. Later, it updates the states based on next observations of the states from measured values by sensors. In general, Kalman Filter ca be described by two steps of measurement update and prediction:

## Prediction 
In this step state transtion function is used to predict the future states
as follows:



## Measurement Update



# Extended Kalman Filter
