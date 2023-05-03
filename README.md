# 2004_simple_simpy_parallel

A simple SimPy hospital model running on parallel cpu cores. The intention is to show a framework for hospital modelling using SimPy with Model, Hospital, and Patient classes, and with scenarios and trials managed by a Replicator class; it is not intended to be a full hospital model itself.

## Running the simulation:

Use `simplest_model_1.ipynb` to revise a simple SimPy model (non-object-oriented), and `simplest_model_2_with_resources.ipynb` to revise how limited resources may be added to a SimPy model.

Use `single_model_run.ipynb` as your starting point to understand the object-oriented odel using a single run of a single sceanrio.

Use `parallel_function.ipynb` to understand parallel processing across CPU cores.

Use `simple_replicate_scenarios_model.ipynb` to see how multiple scenarios may be defined and running with replication across multiple CU cores.

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
    
### Learning objectives

1. Learn how to set up a custom Python environment  (to ensure consistency of package versions) using Anaconda or Python/Pip environments.

2. Revise simple SimPy models, and learn how to structure a simple SimPy simulation using Object Oriented Programming (OOP)

3. Learn how to create a Jupyter Notebook user interface to a model, allowing the user to create multiple sceanrios

4. Learn how to run parallel Python function calls across multiple CPU cores

5. Learn how to run SimPy models with multiple scenarios and replicates (across CPU cores) with a Jupyter Notebook interface

6. Learn how to make you model available  on the web using GitHub and mybinder.org

## Files

### Simple model examples

These are standalone models without parallel processing or scenario handing. These are to illustrate simpy models.

* `simplest_model_1.ipynb`: A standalone model of patients arriving at ED and being seen in order. There are no resources in this model.

* `simplest_model_2_with_resources.ipynb`: A standalone model of patients arriving at ED and being seen in order. This model adds the doctor as a resource.

### Setting up the model for scenarios

Scenarios allow us to pass model parameters to the model, and so may be used to automate running the model with different paramater values.

#### `single_model_run.ipynb`

* This model holds model parameters in a `Scenario` class that is available by loading the `parameters` module from the `sim_classes` package.

* The simulation model is loaded as a class `Model` from the `model` module in the `sim_classes` package. The model itself loads a `Patient` class which is used to create patient objects which hold the priority of the patient, and track the patient through the hospital. The `Hospital` class manages patients through the hospital.

#### parallel_function.ipynb

* This is an example of using `joblib` to run replicates of a function across multiple CPU cores. It does not use SimPy.

#### simple_replicate_scenarios_model.ipynb

* This notebook uses `joblib` to set up and run multiple replicates of a model. It calls the `replication` module from the `sim_classes` package. This module runs the model in parallel multiple times for each scenario, and and collates results.
