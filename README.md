# Machine Learning Model Lifecycle using MLFlow


MLflow is an open source platform for managing the end-to-end machine learning lifecycle. It helps data scientists and ML engineers track and version experiments, package code into reproducible runs, deploy models to production, and monitor performance.

Key capabilities:
* *MLflow Tracking*: Logs parameters, code versions, metrics, and artifacts during model training and validation. This enables you to visualize and compare runs.
* *MLflow Projects*: Packages code and configurations so you can reproduce runs on any platform. Runs can be local or on remote compute clusters.
* *MLflow Models*: Helps deploy machine learning models on diverse serving platforms like TensorFlow, PyTorch, and SageMaker. Has model versioning and stage transitions like staging, production.
* *Model Registry*: Centralized model store to collaboratively manage models and their lifecycle. Integrates with other MLflow components.
* *MLflow UI*: Visualize, compare and search runs, models, artifacts, etc through a user interface.

In summary, MLflow provides end-to-end capabilities to efficiently develop, test, deploy and monitor machine learning models and experiments. It is an essential toolkit for machine learning teams.

#

Files in this repository include:


## 1. Readme
  The `README.md` file is a markdown file that contains basic information about the repository, what files it contains, and how to consume them


## 2. Requirements
  The `requirements.txt` file has a list of packages to be installed for any required project. Currently, my requirements file contains some basic python packages.


## 3. Codes
  This folder contains all the code files used in this repository - the files named "Test_" will be used for testing and the remaining will define certain functions


## 4. Resources
  -  This folder contains any other files relevant to this project. Currently, I have added -


## 5. CI/CD Automation Files


  ### 5(a). Makefile
  The `Makefile` contains instructions for installing packages (specified in `requirements.txt`), formatting the code (using black formatting), testing the code (running all the sample python code files starting with the term *'Check...'* ), and linting the code using pylint


  ### 5(b). Github Actions
  Github Actions uses the `main.yml` file to call the functions defined in the Makefile based on triggers such as push or pull. Currently, every time a change is pushed onto the repository, it runs the install packages, formatting the code, linting the code, and then testing the code functions


  ### 5(c). Devcontainer
  
  The `.devcontainer` folder mainly contains two files - 
  * `Dockerfile` defines the environment variables - essentially it ensures that all collaborators using the repository are working on the same environment to avoid conflicts and version mismatch issues
  * `devcontainer.json` is a json file that specifies the environment variables including the installed extensions in the virtual environment
