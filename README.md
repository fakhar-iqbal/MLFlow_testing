# MLFlow_testing



## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/fakhar-iqbal/MLFlow_testing.mlflow \
MLFLOW_TRACKING_USERNAME=fakhar-iqbal \
MLFLOW_TRACKING_PASSWORD=703df66655cc95b6efa52e5afcf9b38beb771958 \
python script.py


```cmd

set MLFLOW_TRACKING_URI=https://dagshub.com/fakhar-iqbal/MLFlow_testing.mlflow

set MLFLOW_TRACKING_USERNAME=fakhar-iqbal

set MLFLOW_TRACKING_PASSWORD=703df66655cc95b6efa52e5afcf9b38beb771958


```


# MLFLOW ON AWS

## MLFLOW on AWS setup:

1. login to aws console
2. create iam user with admininstartionaccess
3. export the credentials in your aws cli by running "aws configure"
4. create an s3 bucket
5. create ec2 machine (ubuntu) & add security groups 5000 port

Run the ollowing command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell



## then set aws credentials 
aws configure


# Finally
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-test-23

# open public ipv4 dns to the port 5000

#set uri in your local terminal and in your code
export MLFLOW_TRACKING_URI=http://ec2-54-147-36-34.compute-1.amazonaws.com:5000/
```

