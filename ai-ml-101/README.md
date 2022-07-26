# Kubernetes Academy 101: AI/ML

## Deploying Jupyter Notebooks

### What to Expect

We will deploy a Kubernetes cluster using Platform9, deploy hostpath storage, and finally deploy a Jupyter notebook backed by persistent storage.

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
- Access the Notebook using a token.
- Run “Hello, world!” on your Jupyter notebook.
  - Create a new notebook and run Hello, World! Congrats, that was your first notebook on Kubernetes!
- Load an example Tensorflow Tutorial Notebook
  - Run the Notebook and update a section or two.

### Pre-requisites

- BareOS: Bare Metal or VMs running Ubuntu 20.04

- LoadBalancer or NodePort
  - LoadBalancer will require MetalLB being deployed when configuring the cluster.
  - NodePort will not require additional configuration during cluster deployment.

### Kubernetes Benefits

Easily scale up Jupyter notebooks for your users. Give each user access to their own notebook so that they can experiment. Ideally after running a single pod for a Jupyter notebook for testing, we would progress to configuring JupyterHub (<https://zero-to-jupyterhub.readthedocs.io/en/latest/>) to help automate notebooks for our users.

### Deploy a Cluster with Platform9 Free Tier

We are going to start out by deploying a Kubernetes cluster using Platform9.

- Bare Metal: 2-3 Bare Metal Nodes (<https://platform9.com/docs/kubernetes/get-started-bare-metal>)
- VM: with 2-3 Virtual Machines Nodes (<https://platform9.com/docs/kubernetes/get-started-bare-metal>)

![alt text](images/dashboard.png)

We will access the cluster using kubectl, which means we will need to install kubectl (<https://kubernetes.io/docs/tasks/tools/#kubectl>)

### Configure Storage with the CSI HostPath Driver

Now that we have a cluster we will deploy a storage provider so that we can save our work.

This will be done using the App Catalog. The App Catalog will allow us to quickly deploy helm based applications.

![alt text](images/hostpath.png)

### Deploy a Jupyter Notebook

Create a deployment using jupyter/tensorflow-notebook. (<https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html>)

Examples for two methods, one being NodePort and the other being LoadBalancer.

At this point we can either clone the github repository (<https://github.com/Platform9-Community/ai-ml-workshop>) or you can download/copy the jupyter.yaml file from either the NodePort folder or the LoadBalancer folder under the ai-ml-101 directory.

Once you have the file on your machine, or somewhere that can use kubectl to access the cluster, we can run:

`kubectl create -f jupyter.yaml`

### Access the Notebook

Once the notebook has deployed we can pull the logs to figure out the URL + Token. The Tensorflow image is around 1GB so it can take a few moments for the pod to move into a running state. 

Assuming we are deployed in the default namespace, we can view the status of the pod using:

`kubectl get pods -w`

If the original yaml file was modified to use namespaces you would need to specify the namespace:

`kubectl get pods -n NAMESPACE -w`

Once the pod is in a running state we can view the logs:

`kubectl logs jupyter`

### Hello World! Example

Create a new notebook and run Hello World!

```python
print("Hello, World!")
```

### Tensorflow Example Notebook

Download the notebook from (<https://www.tensorflow.org/tutorials/images/classification>)

Download the notebook from (<https://www.tensorflow.org/hub/tutorials/tf2_object_detection>)

Once one of the notebooks have been downloaded we can upload the notebook. At this point we will upload the notebook, open it, and then restart and run the notebook.

There are a couple of helpful commands that we can run when the notebook is working through each section. There are a few sections that will increase the memory and cpu usage. To see what kind of impact this is having on your nodes you can run:

`kubectl top nodes`

