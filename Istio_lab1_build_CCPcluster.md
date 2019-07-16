# ISTIO LEARNING LAB
![alt text][logo]

[logo]: Istio_DNE_Images/istio_banner.png "Logo Title Text 2"

## Objectives
Completion Time: 60 minutes
1. Lab 1: Build a K8s Cluster on CCP
2. Lab 2: Setup Kubernetes CLI on you laptop
3. Lab 3: Instal myhero Application
3. Mission: Istio Traffic Routing
4. Mission: Istio Gradual Migration
5. Mission: Istio Delay Injection
6. Mission: Istio HTTP Abort Injection

In this lab you will learn the basics of using Istio service mesh on a microservices application architecture.


### Prerequisites
Before you attempt this lab it will make much more sense if you have already completed the following modules:
1.	Cisco Container Platform 1.5
2.	Intro to Kubernetes (K8s)
3.	Completed setup and have Kubernetes CLI (kubectl) installed in your local laptop


# Excercise 1: Build a New Kubernetes Cluster on CCP
We need a Kubernetes cluster upon which to run our application. So we will use Cisco Container Platform(CCP) to launch a new cluster for our app.

## Login to CCP
Login to you CCP Sandbox Dashboard https://198.18.1.110 with credentials `admin/Cisco123`

## Create a cluster
Once you are in your CCP admin select you will see the default cluster “sandbox_demo_Cluster-1”. Like in the previous CCP lab we are going to build a new cluster for our application so Click on “New Cluster”

![alt text][newcluster]

[newcluster]:Istio_DNE_Images/CCP_New_Cluster.png "Select New Cluster"



![alt text][CCP_Basic_Info_1]

[CCP_Basic_Info_1]:Istio_DNE_Images/CCP_Basic_Info_1.png "Complete Form"


### Fill out the basic information:
Infrastructure Provider: `vsphere`<br>
Kubernetes Cluster Name: `myhero`<br>
Kubernetes version: `1.12.3`<br>
Container Network Interface: `calico`<br>
Description: `myhero cluster`<br>
Click "Next"

![alt text][CCP_Provider_Settings_2]

[CCP_Provider_Settings_2]:Istio_DNE_Images/CCP_Provider_Settings_3.png "Complete Form"

Data Center: `ccp`<br>
Cluster: `ccp`<br>
Resource Pool: `Resources`<br>
Network: `vmnetwork`<br>
Hyperflex Local Network: ``<leave this blank>``<br>
Datastore: `CCPDatastore`<br>
VM Template: `ccp-tennant-image-1.12.3-ubuntu18-3.1.0`<br>

![alt text][CCP_Node_Conf_3]

[CCP_Node_Conf_3]: Istio_DNE_Images/CCP_Node_Conf_3.png "Complete Form"

Leave the Worker and Master node configurations as default.

VM Username: `ccpuser`<br>
For SSH Public Key, you can use your own ECDSA SSH public key or paste in the key below:

```
ecdsa-sha2-nistp521 AAAAE2VjZHNhLXNoYTItbmlzdHA1MjEAAAAIbmlzdHA1MjEAAACFBAHlSb9ZkXQL5/GI12258c+AIKVhDN1p1VYjvJR5oliqoR/gN/65D04BfsZWE8nk00AtJzvEVbjenwLeWuvIQsFs5AHa5uM4Fpmw3Ylpt1tB/GZHZ5Mg9sh1iLh5agSgNLWkAgCRvySmLO3fSq0IKarnQrMqId2pGUlNZr/YPP4irTvU6w== sandbox@CCP_SANDBOX_NISTP521_KEY
```
Number of Load Balancer IPs: `10`<br>
Subnet:`10.10.20.0/24`<br>
Pod Network CIDR: `192.168.0.0/16`<br>
Root CA Certificate: `<leave this blank>`<br>
Enable Istio: `YES` <This is Important!><br>

Click Next and Next again to get to the summary page and "Finish". Your Cluster will build.

![alt text][CCP_Cluster_Build]

[CCP_Cluster_Build]: Istio_DNE_Images/CCP_Cluster_build.png "building"

Once the Cluster is Ready select `Download Kubeconfig`to access the Kubernetes dashboard.
![alt text][k8s_download_token]

[k8s_download_token]: Istio_DNE_Images/k8s_download_token2.png "Token"

Open the dashboard and select the kubeconfig.yaml file you just downloaded.
![alt text][k8s_token2]

[k8s_token2]: Istio_DNE_Images/k8s_token2.png "Token Input"

You are in and your cluster is up and running.
![alt text][k8s_initial_homepage]

[k8s_initial_homepage]: Istio_DNE_Images/k8s_initial_homepage.png "k8s Homepage"


We are done here.
