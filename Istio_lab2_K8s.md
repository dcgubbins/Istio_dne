# ISTIO LEARNING LAB

![alt text][logo]

[logo]: Istio_DNE_Images/istio_banner.png "Logo Title Text 2"


## Istio Service Mesh#

In this lab you will learn the basics of using Istio service mesh on a microservices application architecture.

## Objectives
Completion Time: 10 minutes
Setup Kubernetes CLI on you laptop


# Lab 2: Setup Your New Cluster
Now we have our cluster running there are a few more steps to complete before we are ready to install our applications

1. Setup Kubectl on the CENTOS machine to remotely control the cluster from your laptop
2. Create a new namespace called myhero for our application
3. Enable Instio sidecar injection within the myhero namespace

##Setup Kubectl on our laptop to remotely control the cluster from your laptop
It is useful to run the K8s CLI from a laptop. This way you can switch between multiple clusters under your control.

Form the CENTOS machine open a terminal window.

Take a look at your K8s CLI current configuration

```
Kubectl config view
```

Example output below
![alt text][kubectl_config_view_2]

[kubectl_config_view_2]:Istio_DNE_Images/kubectl_config_view_2.png "Config View"

This example shows that k8s CLI is already installed and configured to use a local cluster on the laptop called minikube.

There is a kubeconfig file behind every working kubectl command. This file typically lives at $HOME/.kube/config.

There are three ways to point your kubectl to a kubeconfig.

1.  --kubeconfig flag, if specified
2.  use KUBECONFIG environment variable, if specified
3.  $HOME/.kube/config file

Above is thehis is the order of preference that takes effect while determining which kubeconfig file is used.

For our lab we will use option 2 and point to our kubeconfig using using an environment variable pointing to the Kubeconfig/Token you downloaded from your k8s cluster in the previous lab.
```
echo $Home
```
```
export KUBECONFIG=$HOME/Downloads/kubeconfig.yaml
```

Example below
![alt text][Kubectl_switch_context]

[Kubectl_switch_context]:Istio_DNE_Images/KubeconfigENV.png "Config View"

If its successful you should Now be able to control the cluster you just built on CCP.

```
kubectl get nodes
```
You should now see the nodes of the remote cluster.

Well done. Your work here is done!
