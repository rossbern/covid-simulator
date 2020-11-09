# covid-simulation
This code simulates the spread of COVID-19 in New York City with Python. An SIR model is used to track the number of susceptible, infected, and recovered individuals over time. In order to simulate the spread of the virus within NYC specifically, an OD-flow matrix was built using real transit data, which approximates the movement of individuals throughout the city on a typical day. The code was designed to allow for quickly running many simulations in parallel. This was achieved by vectorizing all operations in Numpy and Cython, and utilizing multiprocessing.


## Requirements
The file [environment.yml](https://github.com/rb2540/covid-simulation/blob/main/src/environment.yml) is provided, which can be imported to create the proper conda environment.


## Contents
The code is contained in the following notebooks in the [src](https://github.com/rb2540/covid-simulation/tree/main/src) folder:
* [get_nyc_od_matrix.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/get_nyc_od_matrix.ipynb) contains the code to generate the OD-flow matrix
* [Cython_Optimizations.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Cython_Optimizations.ipynb) details how the code was optimized with cython and multiprocessing
* [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb) provides several examples of how the simulation can be used


## Usage
Simulations can be run with different conditions in order to gain important insights about the virus. For example, we can use the simulation to model the effects of social distancing, or to evaluate different policy decisions. The following plots show how shutting down mass transit one week earlier or later would have affected transmission over time:

![Transit Decline Timing](https://github.com/rb2540/covid-simulation/blob/main/figures/TransitTimingDeclinesPlots.jpg)

Several other examples are provided in [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb). 


