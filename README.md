## Environment Setup (MiniConda)

1. Clone the repository and fetch branches:
   - `git clone --single-branch --branch main https://github.com/trustworthyrobotics/VISION-SLS.git`
   - `cd Safe-Perception-SLS`

2. Create a Conda environment and install dependencies:
   - `conda env create -f safe-percpetion-sls.yml`
   - `pip install -e .`

Note: We only tested the setup in Ubuntu 22 OS and cannot guarantee it will work on other systems. 

The ROS2 code for running hardware experiment is in [this repo](https://github.com/nexuszhan/turtlebot4_ws/tree/main). 

## Introduction to Repo Layout

The dyn directory contains the definitions of dynamics used in the experiments.

The expe directory contains code for running experiments. 
   - main_*.py runs our robust MPC algorithm and saves the plan to a .npz file
   - run_*.py runs the plan in a simulated environment

The perception_utils directory contains functions for percpetion. 

The solver directory contains implementation of our method. 

## Tips

For the first time running our algorithm with parallel double Riccati enabled, the numba function can take some time to compile. 
