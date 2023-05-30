# Kubernetes introduction

It's time to play with [Kubernetes](https://kubernetes.io/)

In this repository you will work through starting a Kubernetes cluster (on your own computer) and getting it to run various [deployments](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/) and [services](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/).

## Pre-requisites

- Completed the [Docker Exercise](https://github.com/northcoders/ce-docker) if you wish to use Docker Desktop to create a Kubernetes cluster

## Scenario

In this guide, you will 

* Create a kubernetes cluster that runs locally on your computer
* Deployment an NGiNX container to the cluster
* Scale that deployment to have multiple containers running
* Expose those containers via a service

You will also build out your knowledge of Kubernetes commands and using the [kubectl](https://kubernetes.io/docs/reference/kubectl/) command line tool.

## Instructions

### Running Kubernetes locally

Before we transition to the cloud (and run Kubernetes on AWS) let's start with running Kubernetes locally on your computer. 

This allows us to play with Kubernetes commands without incurring cloud expenditure.

The first step is to install the kubectl command line tool

**Installing the kubectl tool**

In order to interact with Kubernetes we need a command line tool called **kubectl**

The kubectl tool allows us to interact with the Kubernetes API and instruct your cluster to take different actions.

Follow the corresponding link below to install kubectl

[Linux installation](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)

[Mac installation](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)

[Windows installation](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/)

Once kubectl has been installed it's time to get a kubernetes cluster running locally. There are various options for running kubernetes locally, two are outlined below. Pick one of the options before proceeding.

**Using Docker Desktop to run a kubernetes cluster**

Docker Desktop now comes bundled with an ability to run Kubernetes locally.

Follow the instructions on the Docker website for enabling Kubernetes

[Enabling kubernetes with Docker Desktop](https://docs.docker.com/desktop/kubernetes/)

**Using minikube to run a kubernetes cluster**

[Minikube](https://minikube.sigs.k8s.io/docs/) is another alternative for running a kubernetes cluster locally

The minikube webiste provides a getting started guide for installing minikube

[Minikube getting started guide](https://minikube.sigs.k8s.io/docs/start/)


### Verifying you can access your cluster

Much like you have to configure the AWS command line with authentication information, in order for it to know which AWS account to communicate with, you have to do the same for the **kubectl** command. You have to configure the kubectl with a context in order to know which cluster it is interacting with. 

Both minikube and the docker desktop tool should automatically do this for you. In order to validate whether it has worked, try seeing if you can see the [nodes](https://kubernetes.io/docs/concepts/architecture/nodes/)

Run the command

```
kubectl get nodes
```

You should see output similar to (the name will be different if you are on Mini Kube)

```
NAME             STATUS   ROLES           AGE     VERSION
docker-desktop   Ready    control-plane   3h52m   v1.25.2
```




