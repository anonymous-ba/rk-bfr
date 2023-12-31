Code for the article *"A Bayesian approach to functional regression: theory and computation"*, submitted for publication at the [Bayesian Analysis](https://projecteuclid.org/journals/bayesian-analysis) journal.

---------

# rk-bfr

A Bayesian framework for functional linear and logistic regression models, built on the theory of RKHS's.

## Code structure

- The folder `rkbfr` contains the inference and prediction pipeline implemented, using the [emcee](https://emcee.readthedocs.io/) MCMC sampler and following the style of the [scikit-learn](https://scikit-learn.org/) and [scikit-fda](https://fda.readthedocs.io/) libraries.
- The folder `reference_methods` contains the implementation of some functional algorithms used for comparison.
- The folder `utils` contains several utility files for experimentation and visualization.
- The `experiments` folder contains plain text files with numerical experimental results, as well as `.csv` and `.npz` files that facilitate working with them directly in Python.

## Usage

There are some experiments (with both simulated and real data) available to test the performance of the models against other usual alternatives, functional or otherwise. The script `results_cv.py` runs the experiments with a cross-validation loop for our Bayesian models, while the script `results_all.py` runs the experiments for all hyperparameters without a cross-validation loop. 

A typical execution can be seen in the `launch.sh` file, and additionally there are two Jupyter notebooks that demonstrate the usage of the code.

*Code developed for Python 3.9.*
