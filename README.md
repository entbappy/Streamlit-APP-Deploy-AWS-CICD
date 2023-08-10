# Streamlit-APP-CICD-Deployment-with-Github-Actions-on-AWS

### Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to docker hub

	3. Launch Your EC2 

	4. Pull Your image from docker hub in EC2

	5. Lauch your docker image in EC2

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#Policy:

	1. AmazonEC2FullAccess

	

## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#Install Docker

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker


### Note: Do the port mapping to this port:- 8501
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    DOCKER_PASSWORD

    DOCKER_USERNAME

    IMAGE_NAME

    REGISTRY