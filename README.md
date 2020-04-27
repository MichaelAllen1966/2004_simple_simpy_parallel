# 2004_simple_simpy_parallel

A simple SimPy hospital model running on parallel cpu cores.

## Running the simulation:

Use `single_model_run.ipynb` as your starting point to understand the model using a single run of a single sceanrio.

Use `parallel_function.ipynb` to understand parallel processing across CPU cores.

Use `sim_replicates.ipynb` to see how multiple sceanrios may be defined and running with replication across multiple CU cores>


## Run on BinderHub:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MichaelAllen1966/2004_simple_simpy_parallel/master)

Note: BinderHub is currently limited to one CPU, so there is no advantage of parallel processing on BinderHub.

To set up use of any Python code, using a Jupyter Notebook as the front end, on BinderHub, place the requirements for the code in a `.yml` file in a `binder` subdirectory. Upload code to GitHub. Binder can then run the code from binder.org, which will also give a link for putting a badge in the GitHub READNE.md file.

## Set up environment locally

To get the correct libraries and versions it is recommended that the provided conda environment is used. To create and activate a bootcomp environment:

1. Windows -> Open Anaconda prompt. Mac/linux -> Open a terminal

2. Navigate to the /binder directory

3. Run the following command: `conda env create -f environment.yml`

This will fetch and install the libraries in a conda environment 'simple_sim'

4. To activate the enviroment run the following command:
    `conda activate screening_lab`
