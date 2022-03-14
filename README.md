# Building and Deploying a python application to Docker and Azure App services using Azure CI/CD pipelines

This readme file explains all the processes I employed in automating a CI/CD  
workflow for a python project using Azure DevOps<br/>
This is the almighty formular for DevOps engineers on azure DevOps.

<br/>

## Requirements

1. Azure account.
2. Visual Studio.
3. Azure DevOps account.

## Process Flow Chat
The following steps were followed to deploy a
python app from azure DevOps repo to a docker
Container in docker hub since it's free and an azure app service.

1. Create a resource group.
2. Create a web app in the above resource group
3. Create a service connection to login and connect to docker hub
4. Create another service connection to connect to active directory
5. Create a pipeline, select the repo, it automatically detect the 
kind of application based on the files in the repo. In 
This case a python to Linux webapp on azure was selected.
6. The following steps were added
      -Docker build step to build the dockerfile
      -Docker push step to push the built image to dockehub
      -copy
      -publish
7. The file was saved and run successfully.
NB: I didn't have to create a release pipeline beacsue 
The yml file contained a deploy task which automatically deploys the app to 
Azure web services upon commit to the main branch.
