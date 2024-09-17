# Deployment Of Web App

## Step 1: Create Ubuntu EC2 & Install the Jenkins Server

### Update all software packages on Ubuntu server

### Install Java on Ubuntu server

### Jenkins Installation


## Step 2: Create a Jenkins Pipeline Job 

### Create a Pipeline Job 

Install Stageview plugin from manageJenkins -> Plugins -> Available plugins

## Step 3: Write the code for Sample web app (python)

## Step 4: Containerize the Python app and publish to DockerHub

### Docker Installation


## Step 5: Create Kubernetes Cluster

### Install Kops

### Install kubectl

### AWS CLI Installation

### Create Kubernetes Cluster



## Step 6: Deploy to kubernetes

### Add a new stage in Jenkins file

### Configure Webhook in github & Jenkins

Github Repo Setting -> Webhooks -> http://43.205.203.11:8080/github-webhook/
Jenkins Job -> Build Triggers -> GitHub hook trigger for GITScm polling

### Make a Commit & Run the Deployment

If you commit then jenkins will automatically start the pipeline job.
