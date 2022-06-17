# What is Helm?

Helm is a Kubernetes deployment tool for automating creation, packaging, configuration, and deployment of applications and services to Kubernetes clusters. In other words, Helm is a package manager for Kubernetes. It deploys `charts`, which you can think of as a packaged application. The package is a collection of all your versioned, pre-configured application resources which can be deployed as one unit.

# Why should you use Helm?

## Saves time

Instead of having to write separate YAML files for each application manually, you can simply create a Helm chart and let Helm deploy the application to the cluster for you. 

## Ability to rollback

Helm automatically maintains a database of all the versions of your releases. So, whenever something goes wrong during deployment, rolling back to the previous version is just one command away.

## Ease of use

Once the chart has been built, it can be easily used by anyone. However, setting up the chart itself is not trivial and time will need to be invested in going through Helm's extensive documentation.

# Understanding the chart's file system

The three important files to pay attention to are `values.yaml`, `deployment.yaml`, and `service.yaml`. You can create variables in `values.yaml`, which can then be accessed in the other two files to set up the various components of Kubernetes. For example, if you set up `app_name: eng110-node-deployment` as a variable in `values.yaml`, then you would access it in the other yaml files by using this syntax: `{{ .Values.app_name }}`.

# Using this Helm repository

To use this Helm repository, make sure you first have Helm installed with these commands:

> 1. Download Helm with `curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3`.
> 2. Make the file executable with `chmod 700 get_helm.sh`.
> 3. Run the script with `./get_helm.sh`.

More comprehensive documentation for helm installation across different operating systems can be found [here](https://helm.sh/docs/intro/install/).

Once Helm is installed, you can add this repository with the command `helm repo add custom-name-here https://samuel-walters.github.io/eng110-helm/`. To then install the chart, you should then run the command `helm install custom-name-here custom-name-here/eng110-nodeapp`. 

# Setting up your own Helm repository.

Please click [here](https://github.com/samuel-walters/Complete-CICD/blob/main/Set_Up_Helm_Repository.md) to view documentation for how to set up your own Helm repository on GitHub.
