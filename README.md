# 2004_simple_simpy_parallel

A simple SimPy hospital model running on parallel cpu cores. The intention is to show a framework for hospital modelling using SimPy with Model, Hospital, and Patient classes, and with scenarios and trials managed by a Replicator class; it is not intended to be a full hospital model itself.

## Running the simulation:

Use `simplest_model_1.ipynb` to revise a simple SimPy model (non-object-oriented), and `simplest_model_2_with_resources.ipynb` to revise how limited resources may be added to a SimPy model.

Use `single_model_run.ipynb` as your starting point to understand the object-oriented odel using a single run of a single sceanrio.

Use `parallel_function.ipynb` to understand parallel processing across CPU cores.

Use `sim_replicates.ipynb` to see how multiple sceanrios may be defined and running with replication across multiple CU cores>

Please also see `Additional models` folder for further model examples (e.g. including plotting results).


## Run on BinderHub:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MichaelAllen1966/2004_simple_simpy_parallel/master)

Note: BinderHub is currently limited to one CPU, so there is no advantage of parallel processing on BinderHub.

To set up use of any Python code, using a Jupyter Notebook as the front end, on BinderHub, place the requirements for the code in a `.yml` file in a `binder` subdirectory. Upload code to GitHub. Binder can then run the code from binder.org, which will also give a link for putting a badge in the GitHub READNE.md file.

## Set up environment locally

To get the correct libraries and versions it is recommended that the provided conda environment is used. To create and activate the environment:

### Using Anaconda

1. Windows -> Open Anaconda prompt. Mac/linux -> Open a terminal

2. Navigate to the /binder directory

3. Run the following command: `conda env create -f environment.yml`

This will fetch and install the libraries in a conda environment 'simple_sim'

4. To activate the enviroment run the following command:
    `conda activate simple_sim`
    
### Using Python environments

1. Navigate to the main project folder (unless you prefer to build your Python environments elsewhere.

2. Open a terminal/command line, and type `python3 -m venv venv`

3. Activate your environment with `source .\venv\bin\activate`

4. Install requirements with `pip install -r requirements.txt`

### Learning objectives

1. Learn how to set up a custom Python environment  (to ensure consistency of package versions) using Anaconda or Python/Pip environments.

2. Revise simple SimPy models, and learn how to structure a simple SimPy simulation using Object Oriented Programming (OOP)

3. Learn how to create a Jupyter Notebook user interface to a model, allowing the user to create multiple sceanrios

4. Learn how to run parallel Python function calls across multiple CPU cores

5. Learn how to run SimPy models with multiple scenarios and replicates (across CPU cores) with a Jupyter Notebook interface

6. Learn how to make you model available  on the web using GitHub and mybinder.org
