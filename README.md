# Capstone

# Things that applied in this project:
* Working in AWS
* Using  Circle CI to implement Continuous Integration and Continuous Deployment
* Building pipelines
* Deploy clusters
* Building Kubernetes clusters
* Building Docker containers in pipelines

# Stages

* lint : lint the app.py and hadolint dockerfile and setup tools for that
* build-docker : building docker container and copy files to it and launch app eventually 
* create-small-cluster : create kubernetes cluster in aws using aws-eks tool
* deploy-cluster : use deployment.yml file to deploy docker image to pods of the cluster 

# In this project Circleci orbs has been used:
* aws-eks: circleci/aws-eks@1.1.0
* kubernetes: circleci/kubernetes@0.12.0
* slack: circleci/slack@4.1

# Files explanation to run app locally

* .circleci : CircleCI config script.
* model_data : Directory with the model data.
* output_txt_files  :<br /> 
     Includes output files of the project :<br />
         1 - Docker_out.txt -> run_docker.sh output.<br />
         2 - Kubernetes_out.txt -> run_kubernetes.sh output.<br />
* app.py : Python application.
* Dockerfile : Docker configuration.
* make_prediction.sh : Pass payload to app.py.
* Makefile : Install, test and lint.
* requirements.txt : Application's dependencies.
* run_docker.sh : Shell script to build and run docker container .
* run_kubernetes.sh : Shell script to run kubernetes with the container from docker hub .
* upload_docker.sh : Shell script to upload image to docker Hub .
