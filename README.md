# Setup of IEM Pro in Azure  Kubernetes Service (AKS)

- [Description](#description)
    - [Overview](#overview)
- [Prerequisites & important details](#prerequisites--important-details)
- [Cluster creation](#cluster-creation)
- [IEM Pro set up](#set-up-iem-pro-on-aks)
- [Contribution](#contribution)
- [License and legal information](#license-and-legal-information)
- [Relevant links](#relevant-links)

## Description

### Overview

This is a short how-to guide to setup an IEM Pro in Azure Cloud via Azure Kubernetes Service (AKS).

AKS is a managed service that lets you run Kubernetes clusters in the Azure Cloud without handling the complex setup and maintenance yourself.

## Prerequisites & important details

- Basic knowledge of Industrial Edge.
- Basic knowledge of the [Azure Portal](https://portal.azure.com/) and the [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/)
- Access to the [Azure Portal](https://portal.azure.com/) and an account with the required permissions  
  (This includes the creation of a resource group, the creation of an aks cluster)

> **_Notice_**:  
Throughout this guide values of CLI paramaters, that are set using environment variables  
e.g. `--parameter $VARIABLE` can be freely changed.  
Filenames that have to be provided will be highlighted using `<` and `>`  
e.g. `--input-file <myfile.txt>`

## Cluster creation

Information regarding the creation of the AKS cluster in Azure can be found in the [cluster](/docs/aks_cluster.md) documentation. Other steps to facilitate the installation process will also be handled here:

- [Launching Azure Cloud Shell](/docs/aks_cluster.md#launching-azure-cloud-shell)
- [AKS cluster creation](/docs/aks_cluster.md#aks-cluster-creation)
- [Creation of a jumphost VM to access the cluster](/docs/aks_cluster.md#creation-of-a-jumphost-vm-to-access-the-cluster)
- [Setup of the jumphost VM](/docs/aks_cluster.md#setup-of-the-jumphost-vm)
- [Setup of an Storage account for file transfer](/docs/aks_cluster.md#setup-of-an-storage-account-for-file-transfer)

## Set up IEM Pro on AKS

After creating the cluster, the IEM Pro can be set up by following the steps in the [installation](/docs/installation.md) section.

- [Ingress Controller Deployment](/docs/installation.md#ingress-controller-deployment)
- [Generate Certificates for the FQDN of your ingress](/docs/installation.md#generate-certificates-for-the-fqdn-of-your-ingress)
- [Create an IEM instance in the IEHub](/docs/installation.md#create-an-iem-instance-in-the-iehub)
- [Installation of the IEM instance](/docs/installation.md#installation-of-the-iem-instance)
- [Setup and apply Ingress](/docs/installation.md#setup-and-apply-ingress)

## Contribution

Thank you for your interest in contributing. Anybody is free to report bugs, unclear documentation, and other problems regarding this repository in the Issues section.
Additionally everybody is free to propose any changes to this repository using Pull Requests.

If you haven't previously signed the [Siemens Contributor License Agreement](https://cla-assistant.io/industrial-edge/) (CLA), the system will automatically prompt you to do so when you submit your Pull Request. This can be conveniently done through the CLA Assistant's online platform. Once the CLA is signed, your Pull Request will automatically be cleared and made ready for merging if all other test stages succeed.

## License and legal information

Please read the [legal information](/LICENSE.md).

## Disclaimer

This documentation describes how you can download and set up a test environment which consists of or contains third-party software.
Please read the following disclaimer carefully: [third-party software disclaimer](/Disclaimer_Tutorials.md)

## Relevant links

<https://portal.azure.com/#home>

<https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli>

<https://learn.microsoft.com/en-us/azure/application-gateway/tutorial-ingress-controller-add-on-new#code-try-0>

<https://learn.microsoft.com/en-us/azure/aks/cluster-autoscaler?tabs=azure-cli>

<https://learn.microsoft.com/en-us/azure/aks/upgrade-aks-cluster?tabs=azure-cli#check-for-available-aks-cluster-upgrades>