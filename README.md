# covid-simulation
This code simulates the spread of COVID-19 in New York City with Python. An SIR model is used to track the number of susceptible, infected, and recovered individuals over time. In order to simulate the spread of the virus within NYC specifically, an OD-flow matrix was built using real transit data, which approximates the movement of individuals throughout the city on a typical day. The code was designed to allow for quickly running many simulations in parallel. This was achieved by vectorizing all operations in Numpy and Cython, and utilizing multiprocessing.

## Usage
Different conditions can be applied to observe how mobility patterns and social distancing affect transmission rates. We can also use the simulation to determine the affects of different policy decisions. Several examples are provided in [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb). 

The code is contained in the following notebooks in the [src](https://github.com/rb2540/covid-simulation/tree/main/src) folder:
* [get_nyc_od_matrix.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/get_nyc_od_matrix.ipynb) contains the code to generate the OD-flow matrix
* [Cython_Optimizations.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Cython_Optimizations.ipynb) details how the code was optimized with cython and multiprocessing
* [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb) shows several ways we can utilize the simulation to answer important questions
