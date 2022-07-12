# Kubernetes Academy Level 101: Deploying Jupyter Notebooks on Kubernetes

## What to Expect from this Workshop

- Kubernetes benefits for Machine learning
  - Go over benefits for Machine Learning. Scaling / Reproducibility / transportability
- Deploy a cluster on Platform9’s Managed Kubernetes Free Tier
  - We will deploy a BareOS Cluster
        - > Platform9 uses the term ‘BareOS’ to refer to a set of physical or virtual machines in your on-premises infrastructure that have a supported linux operating system installed that can be used to create an on-premises Kubernetes cluster.
- Configuring cluster storage with the CSI HostPath driver
  - Deploy with App Catalog
- Deploying a Jupyter notebook in your Kubernetes cluster
  - Deploy with the default container (<https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html>)
- Get information about the notebook using Kubernetes commands.
  - `kubectl logs container`
- “Hello, world” with your Jupyter notebook
  - Create a new notebook and run Hello, World. Congrats, that was your first notebook on Kubernetes! 

## Pre-requisites

- Bare Metal: 2-3 Bare Metal Nodes (<https://platform9.com/docs/kubernetes/get-started-bare-metal>)
- VM: with 2-3 Virtual Machines (<https://platform9.com/docs/kubernetes/get-started-bare-metal>)

## Kubernetes Benefits

Easily scale up Jupyter notebooks for your users. Give each user access to their own notebook so that they can experiment.

## Deploy a Cluster using Platform9

We are going to start out by deploying a Kubernetes cluster using Platform9.

## Configure Storage with the CSI HostPath Driver

## Deploy a Jupyter Notebook

## Access the Notebook

## Hello World! Example
