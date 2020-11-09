# covid-simulation
This is a tool for simulating the spread of COVID-19 within New York City. This was developed in April 2020, shortly after confirmed cases began to spike in NYC. At the time, the transmission and recovery characteristics of the virus were still somewhat unclear, making it difficult to generate reliable predictions using prior research alone. Additionally, data collected from other cities wouldn't necessarily apply to NYC, as the transmission rate is also dependent upon local mobility patterns. The motivation for this project was thus to be able to gather insights about the virus, using rior research where available, and filling in any gaps with simulated data. By running a large number of simulations, we could at least generate likely ranges for the important values. The code was designed to allow for the fast computation of smany simulations in parallel. This was achieved by vectorizing all operations in Numpy, and utilizing Cython and multiprocessing.

The simulation is based on a variation of the SIR model, which tracks the number of susceptible, infected, and recovered individuals over time. In order to accurately simulate the local transmission characteristics within NYC, transit data was used to build an origin-destination matrix, which approximates the movement of individuals throughout the city on a typical day. The incorporation of this matrix provides an additional variable that controls mobility patterns over time. This variable can also be used to encode the effects of social distancing and mandatory quarantines. 


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

