# ISTIO LEARNING LAB

![alt text][logo]

[logo]: /Users/rdickins/Desktop/Istio_DNE_Images/Istio_banner.png "Logo Title Text 2"

<!-- TOC -->
## Istio Service Mesh#

In this lab you will learn the basics of using Istio service mesh on a microservices application architecture.

## Objectives
Completion Time: 60 minutes
1. Build a K8s Cluster on CCP
2. Inatall myhero app on K8s cluster
3. Istio Traffic Routing
4. Istio Gradual Migration
5. Istio Delay Injection
6. Istio HTTP Abort Injection

### Prerequisites
Before you attempt this lab it will make much more sense if you have already completed the following modules:
1.	Cisco Container Platform 1.5
2.	Intro to Kubernetes (K8s)
3.	Completed setup and have Kubernetes CLI (kubectl) installed in your local laptop

# Build a New k8s Cluster on CCP

During the lab we will deploy an application called myhero. We will use a combination of the K8s Dashboard and K8s Command Line (Kubectl).
The reason being you cannot do everything from the Dashboard yet.

##Logon to CCP
Log onto you CCP1.5 Sandbox and open up the kubernetes Dashboard https://10.10.20.30:30894 with credentials `admin/Cisco123`

Once you are in your CCP admin select you will see the default cluster “sandbox_demo_Cluster-1”. Like in the previous CCP lab we are going to build a new cluster for our application so Click on “New Cluster”

![alt text][newcluster]

[newcluster]:  /Users/rdickins/Desktop/Istio_DNE_Images/CCP_New_Cluster.png "Select New Cluster"

