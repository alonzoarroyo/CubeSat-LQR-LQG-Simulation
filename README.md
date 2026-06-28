# CubeSat-LQR-LQG-Simulation
## Project overview
Design and simulation of a Set-Point LQR/LQG controller for a CubeSat in Matlab and Simulink. The system takes roll-pitch-yaw angles as command inputs, translating to reaction wheel motor voltages, and then outputing the attitude(roll-pitch-yaw angles) of the CubeSat.The controller uses a Kalman filter to estimate system states with known proess and measurement noise covarienace matrices, resulting in a smooth output. 
### System States Description
There are 12 states to the CubeSat system, 4 groups of 3, with each group having a member state corresponding to the roll-pitch-yaw angles of the CubeSat:\
$x(1-3)$: Reaction wheel angular velocities\
$x(4-6)$: Reaction wheel currents\
$x(7-9)$: CubeSat angular velocities\
$x(10-12)$: CubeSat angular orientation
## How to Use
1. Clone this repository.
2. Open MATLAB and run `CubeSat_LQR.m` to create matrices in workspace.
3. Open Simulink and run `CubeSat_LQR_simu.slx`.
4. The scope at the system outputs should have angles that match the inputed CubeSat angles.

