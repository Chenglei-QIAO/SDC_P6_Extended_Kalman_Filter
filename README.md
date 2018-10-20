# Extended Kalman Filter Project
## Basics
This project is the 1st project in Term 2 of the Udacity Self-Driving Car Engineer Nanodegree Program. The goal of the project is to implement extended kalman filter to estimate the state of a moving object with noisy lidar and radar measurements. 
## Contents  
The project code are mainly contained in the `src` folder  

  * `main.cpp` - communicates with Term 2 Simulator receiving data measurements, calls a function to run the Kalman filter, calls a function to calculate RMSE(root mean squared error)
  * `FusionEKF.cpp` - initializes the filter, calls the predict function, calls the update function
  * `kalman_filter.cpp` - defines the predict function, the update function for lidar, and radar
  * `tools.cpp` - function to calculate RMSE and the Jacabian matrix.

## Environment Setup
This project involves the Term 2 Simulator which can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases)  
Also, this project involves using an open source package called [uWebSocketIO](https://github.com/uNetworking/uWebSockets).This package facilitates the connection between the simulator and code. The package does this by setting up a web socket server connection from the C++ program to the simulator, which acts as the host.  
The tips for setting up the environment with uWebSockerIO can be found [here](https://classroom.udacity.com/nanodegrees/nd013/parts/40f38239-66b6-46ec-ae68-03afd8a601c8/modules/0949fca6-b379-42af-a919-ee50aa304e6a/lessons/f758c44c-5e40-4e01-93b5-1a82aa4e044f/concepts/23d376c7-0195-4276-bdf0-e02f1f3c665d)
## Build instructions
Once the install for uWebSocketIO is complete, the main program can be built and run by doing the following from the project top directory. 

1. make a build directory: `mkdir build`
2. navigate to the build folder: `cd build`
3. compile: `cmake ..&&make`
4. run it: `./ExtendedKF`
5. run the Term 2 Simulator and visualize the result.

## Results
In the simulation, my EKF produces the following results:  

+ Test with Dataset 1

  Param |  RMSE
  :---: | :----:
  px    | 0.0973
  py    | 0.0855
  vx    | 0.4513
  vy    | 0.4399

+ Test with Dataset 2

  Param |  RMSE
  :---: | :----:
  px    | 0.0726
  py    | 0.0965
  vx    | 0.4216
  vy    | 0.4932

We can see that for both tests, `px,py,vx,vy` output coordinates have an `RMSE < [.11, .11, 0.52, 0.52]`, which turns out that my EKF works well.




