# Hermes chart for Kubernetes deployment

Kubernetes (K8s), is an open-source system for automating deployment, scaling, and management of containerized applications. You can run a Hermes instance inside your Kubernetes cluster, either for testing or production deployments.

## Getting started

First of all, you will need a Kubernetes cluster up and running. If you are not familiar with how Kubernetes works or need some help with this step, please check the [Kubernetes documentation](https://kubernetes.io/docs/home/).

### Install kubectl

`kubectl` is the most commonly used CLI to manage a Kubernetes cluster. The installation instructions are available [here](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

## Deploy Hermes using Helm

Helm works as a package manager to run pre-configured Kubernetes resources. Using our Helm chart you will be able to deploy a Hermes instance in you Kubernetes cluster, with several customizable configurations.

### Install helm

Helm CLI is a Command Line Interface which will automate chart management and installation on your Kubernetes cluster. To install Helm, follow the [Helm installation instructions](https://helm.sh/docs/intro/install/).

The [Parameters](./hermes/README.md#Parameters) section lists the parameters that can be configured during installation.

### Install Hermes chart

#### Through helm v3+

```shell
helm repo add hermes https://runhermes.github.io/charts

helm install myhermes hermes/hermes
```

#### From git

Clone this repository and install the chart

```shell
git clone https://github.com/runhermes/charts.git
cd charts
# Replace <your-release-name> with the name you would like to give to your service
helm install <your-release-name> hermes
```

### Uninstalling the Chart

To uninstall/delete the Hermes release:

```shell
# Replace <your-release-name> with the name of your deployed service
helm uninstall <your-service-name>
```
