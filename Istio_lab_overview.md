![alt text][logo]

[logo]: Istio_DNE_Images/Istio_banner.png "Logo Title Text 2"
# ISTIO LEARNING LAB
<br>
### Prerequisites
Before you attempt this lab it will make much more sense if you have already completed the following modules:
1.	Cisco Container Platform 1.5
2.	Intro to Kubernetes (K8s)
3.	Completed setup and have Kubernetes CLI (kubectl) installed in your local laptop

## Objectives

Completion Time: 90 minutes
1. LAB 1: Build a K8s Cluster on CCP
2. LAB 2: Setup Kubernetes CLI on you laptop
3. LAB 3:Instal myhero Application
3. Mission: Istio Traffic Routing
4. Mission: Istio Gradual Migration
5. Mission: Istio Delay Injection
6. Mission: Istio HTTP Abort Injection

In this lab you will learn the basics of using Istio service mesh on a microservices application architecture.

The full stack reflect the diagram below. We will be using Cisco Container Platform (CCP) to host our K8s clusters and application.

![alt text][Istio_lab_overall_architecture]

[Istio_lab_overall_architecture]: Istio_DNE_Images/Istio_lab_overall_architecture.png "Full Stack"

We will use a combination of the Kubernetes Dashboard and Kubernetes Command Line (Kubectl) to deploy the application and then run through some exercises using ISTIO to manage and control application behaviour.

Istio has a number of capabilities but for these labs the focus will be on Connect and Control.

![alt text][Istio]

[Istio]: Istio_DNE_Images/Istio.png "Full Stack"





Lets Get Started!
