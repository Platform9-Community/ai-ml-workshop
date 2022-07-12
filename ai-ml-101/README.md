# Kubernetes Academy Level 101: Deploying Jupyter Notebooks on Kubernetes

## Syllabus

1. Kubernetes benefits for Machine learning
    1. Go over benefits for Machine Learning. Scaling / Reproducibility / transportability
2. Deploy a cluster on Platform9’s Managed Kubernetes Free Tier
    1. We will deploy a BareMetal or VM cluster
3. Configuring cluster storage with the CSI Hostpath driver
    1. Deploy with App Catalog
4. Deploying a Jupyter notebook in your Kubernetes cluster
    1. Deploy with the default container (https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html)
5. Get information about the notebook using Kubernetes commands.
    1. Kubectl logs container
6. “Hello, world” with your Jupyter notebook
    1. Create a new notebook and run Hello, World. Congrats, that was your first notebook on Kubernetes! 


## Kubernetes Benefits

Easily scale up Jupyter notebooks for your users. Give each user access to their own notebook so taht they can experiment.

## Deploy a Cluster using Platform9

We are going to start out by deploying a Kubernetees cluster using Platform9. 

There are a couple options for cluster sizes. 

> Platform9 uses the term ‘BareOS’ to refer to a set of physical or virtual machines in your on-premises infrastructure that have a supported linux operating system installed that can be used to create an on-premises Kubernetes cluster. 

1. Baremetal: 2-3 Baremetal Nodes (https://platform9.com/docs/kubernetes/get-started-bare-metal)
2. VM: with 2-3 Virtual Machines (https://platform9.com/docs/kubernetes/get-started-bare-metal)
3. VM on Local Machine: All in One (https://platform9.com/docs/kubernetes/get-started-pmk-ova)

## Configure Storage with the CSI Hostpath Driver

## Deploy a Jupyter Notebook

## Access the Notebook

## Hello World! Example