# Real-Estate-Price-Prediction-System

Install ZenML - https://docs.zenml.io/getting-started/installation 

pip install -r requirements.txt


The project can only be executed with a ZenML stack that has an MLflow experiment tracker and model deployer as a component. Configuring a new stack with the two components are as follows:

zenml integration install mlflow -y

zenml experiment-tracker register mlflow_tracker --flavor=mlflow

zenml model-deployer register mlflow --flavor=mlflow

zenml stack register local-mlflow-stack -a default -o default -d mlflow -e mlflow_tracker --set
