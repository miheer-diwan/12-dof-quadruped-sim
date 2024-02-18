# 12 DOF Quadruped Robot Simulation

## Tools Used:
  1. SolidWorks
  2. ROS
  3. Gazebo
  4. Python
  5. C++

## Methodology:
**CAD Modeling:**
* The robot's CAD model was crafted using SolidWorks and exported as a URDF (Unified Robot Description Format).
* The URDF model was then integrated into Gazebo for simulation and testing.

**Control Mechanism:**
* Joint effort controllers were implemented for each joint of the robot.
* PID controllers were employed to regulate the position of each joint, ensuring precise and stable control.

**Home Configuration and Screw Axis:**
* The home configuration for each leg was determined.
* Screw axis parameters for each joint of the robot were calculated to define their rotational behavior.

**Kinematics:**
* Forward Kinematics: Calculated for each leg using screw theory to determine the end effector position.
* Analytical Jacobian: Computed to analyze the robot's motion and velocity.

**Inverse Kinematics:**
* Inverse kinematics for each leg were solved using the Levenberg-Marquardt algorithm, enabling the determination of joint configurations for desired end effector positions.

**Motion Types:**
* Four distinct motion types were defined: forward, backward, left, and right.
* These motions were executed using a trot gait, involving diagonally opposite legs moving simultaneously.

**Trajectory Planning:**
* The trajectory of the end point of each leg was calculated based on current and next foothold positions.
* Transfer time of the feet was considered, and the trajectory followed a sinusoidal path concerning the ground, utilizing the initial foot position as the reference frame.
* A quintic polynomial was employed to compute the horizontal position of the foot during the transfer phase. This implementation allowed translation in all four directions, enhancing the robot's maneuverability.


## Output Video:
https://github.com/miheer-diwan/12-dof-quadruped-sim/assets/79761017/2b617f04-26e8-4576-b80c-26cd9738531f




