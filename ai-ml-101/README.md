# Kubernetes Academy 101: AI/ML

## Deploying Jupyter Notebooks

### What to Expect

We will deploy a Kubernetes cluster using Platform9, deploy HostPath storage, and finally deploy a Jupyter notebook backed by persistent storage.

### Action Items

- Benefits for Machine Learning.
- Deploy a cluster with Platform9 Free Tier.
  - We will deploy a BareOS Cluster
    > Platform9 uses the term ‘BareOS’ to refer to a set of physical or virtual machines in your on-premises infrastructure that have a supported linux operating system installed that can be used to create an on-premises Kubernetes cluster.
- Configure cluster storage with the CSI HostPath driver.
  - Deploy using the App Catalog.
- Deploying a Jupyter notebook in your Kubernetes cluster.
  - Deploy with the default container (<https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html>)
- Get information about the notebook using Kubernetes commands.
  - `kubectl logs container`
- Access the notebook and set a password using the TOKEN from the container.
- Run “Hello, world” on your Jupyter notebook.
  - Create a new notebook and run Hello, World. Congrats, that was your first notebook on Kubernetes!

### Pre-requisites

- Bare Metal: 2-3 Bare Metal Nodes (<https://platform9.com/docs/kubernetes/get-started-bare-metal>)
- VM: with 2-3 Virtual Machines (<https://platform9.com/docs/kubernetes/get-started-bare-metal>)

### Kubernetes Benefits

Easily scale up Jupyter notebooks for your users. Give each user access to their own notebook so that they can experiment.

### Deploy a Cluster with Platform9 Free Tier

We are going to start out by deploying a Kubernetes cluster using Platform9.

We will access the cluster using kubectl.

### Configure Storage with the CSI HostPath Driver

Now that we have a cluster we will deploy a storage provider so that we can save our work.

This will be done using the App Catalog.

### Deploy a Jupyter Notebook

Create a deployment using jupyter/base-notebook.

Examples for two methods, one being NodePort and the other being LoadBalancer.

### Access the Notebook

View the logs from the container so that we can pull the token needed to login.

### Hello World! Example

Create a new notebook and run Hello World!
