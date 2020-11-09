# covid-simulation
This project simulates the spread of COVID-19 in New York City with Python. The code was optimized to run many simulations quickly by vectorizing all operations in Numpy, and utilizing Cython and multiprocessing. In order to simulate the virus' spread in NYC, an OD-flow matrix was built from transit data that models the typical mobility patterns of New Yorkers. 

The code is contained in the following notebooks in the src folder:
* get_nyc_od_matrix.ipynb contains the code to generate the OD-flow matrix
* Cython_Optimizations.ipynb details how the code was optimized with cython and multiprocessing
* Experiments.ipynb details the applications of the simulation model, and tests the effects that different policy decisions could have had on the transmission of the virus.
