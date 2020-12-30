# covid-simulation

<p align="left">
    <img src="figures/TransitTimingDeclinesPlots.jpg" width="1000">
</p>


## Introduction
This is a model designed to accurately simulate the spread of COVID-19 in New York City by utilizing real transit data along with an SIR epidemiological model.  The code uses Cython and multiprocessing for fast computation.

This was developed in April 2020, shortly after COVID-19 cases began to spike in NYC, and it allowed for an early estimation of transmission rates amidst a lack of reliable data.

MTA transit data was used to build an origin-destination matrix, which approximates the movement of individuals throughout the city on a typical day. The incorporation of this matrix introduces an additional variable to the SIR model that controls mobility patterns over time, and can also be used to simulate social distancing or the effects of various policy decisions. 


## Requirements
This project was developed in Python 3. The [environment.yml](https://github.com/rb2540/covid-simulation/blob/main/src/environment.yml) file creates a conda environment called covidsim with all the necessary packages.


## Contents
The code is contained in the following jupyter notebooks in [src](https://github.com/rb2540/covid-simulation/tree/main/src):
* [get_nyc_od_matrix.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/get_nyc_od_matrix.ipynb) generates the origin-destination matrix
* [Cython_Optimizations.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Cython_Optimizations.ipynb) details how the code was optimized with cython and multiprocessing
* [Experiments.ipynb](https://github.com/rb2540/covid-simulation/blob/main/src/Experiments.ipynb) provides several examples of how the simulation can be used


