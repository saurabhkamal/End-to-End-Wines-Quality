# End-to-End-Wines-Quality

## Workfows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the app.py


# How to run?
### Steps:

clone the repository

```bash
https://github.com/saurabhkamal/End-to-End-Wines-Quality
```

### STEP 1: Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.10 -y
```

```bash
conda activate mlproj
```

### STEP 2: install the requirements
```bash
pip install -r requirements.txt
```

### Step before deployment
```bash
python app.py
app -> http://localhost:8080/
```


# AWS-CI-CD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

    #with specific access

    1. EC2 access: It is virtual machine

    2. ECR: Elastic Container registry to save you docker image in aws

    #Description: About the deployment

    1. Build the docker image of the source code
    
    2. Push your docker image to ECR

    3. Launch your EC2  

    4. Pull your image from ECR in EC2

    5. Launch your docker image in EC2

    #Policy:

    1. AmazonEC2ContainerRegistryFullAccess

    2. AmazonEC2FullAccess

## 3. Create ECR repo to store/save docker image
    - Save the URI: 566801649228.dkr.ecr.eu-west-2.amazonaws.com/mlproj

    

## 4. Create EC2 machine (Ubuntu)

## 5. Open EC2 and Install docker in EC2 Machine:

    #optional

    sudo apt-get update -y

    sudo apt-get upgrade

    #required

    curl -fsSL https://get.docker.com -o get-docker.sh

    sudo sh get-docker.sh

    sudo usermod -aG docker ubuntu

    newgrp docker

    docker --version

## 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one

## 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = eu-west-2

    AWS_ECR_LOGIN_URI = demo>>

    ECR_REPOSITORY_NAME = simple-app


