# covid-simulation
This repo contains Python code to simulate the spread of COVID-19 in New York City. This tool was developed in April 2020, shortly after COVID-19 cases began to spike in NYC. The simulation is based on a variation of the SIR model, which tracks the number of susceptible, infected, and recovered individuals over time. In order to accurately simulate the local transmission characteristics within NYC, transit data was used to build an origin-destination matrix, which approximates the movement of individuals throughout the city on a typical day. The incorporation of this matrix builds upon the traditional SIR model by providing an additional variable that controls urban mobility patterns over time. This variable can also be used to encode the effects of social distancing and mandatory quarantines. 

The code was designed to allow for the fast computation of several simulations in parallel. This was achieved by vectorizing all operations in Numpy, and utilizing Cython and multiprocessing.


## Requirements
The file [environment.yml](https://github.com/rb2540/covid-simulation/blob/main/src/environment.yml) is provided, which can be imported to create the proper conda environment.


## Contents
The code is contained in the following jupyter notebooks in [src](https://github.com/rb2540/covid-simulation/tree/main/src):
* [get_nyc_od_matrix.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/get_nyc_od_matrix.ipynb) generates the origin-destination matrix
* [Cython_Optimizations.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Cython_Optimizations.ipynb) details how the code was optimized with cython and multiprocessing
* [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb) provides several examples of how the simulation can be used


## Usage
The code allows for simulations to be run with varying conditions, in order to gain insights and answer important questions about the virus. For example, we can use the simulation to model the effects of social distancing, or to evaluate different policy decisions. The following plots show how shutting down mass transit one week earlier or one week later would have affected transmission over time:

![Transit Decline Timing](https://github.com/rb2540/covid-simulation/blob/main/figures/TransitTimingDeclinesPlots.jpg)

Several other examples are provided in [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb). 


## Report
This [report]() accompanied the project as a part of

