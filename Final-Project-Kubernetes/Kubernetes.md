# Kubernetes: A Containerization Orchestration Tool

## Terminology
Containerization - packaging of an application and its dependencies into essentially a lightweight VM

Cluster - components that represent the control pane, a set of nodes

Nodes - set of machines orchestrated by Kubernetes

Pods - components of the application workload

Pods --> Containers --> Nodes --> Cluster

## Purpose
(https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/)

Kubernetes is made to run applications in a distributed fashion to maximize resilience from unexpected events that could otherwise inhibit functionality. 

Kubernetes is commonly used for... 

Service discovery: containers can be exposed using a DNS name or by their own IP address 

Load balancing: can automatically distribute traffic across pods in order to maintain a deployment’s stability 

Storage orchestration: automatically mounts a storage system based on the user’s preferences. For example, local storage, the cloud, etcetera. 

Automated rollouts and rollbacks: like Netflix’s Red-Black strategy, Kubernetes allows you to automatically deploy containers to replace old containers at a controlled rate, and vice versa for rollbacks. 

Automatic bin packing: the user can provide a cluster of nodes to run containerized tasks, and each container is fit onto the nodes in such a way that maximizes resource efficiency in terms of CPU and RAM 

Self-healing: restarts containers that fail, replaces containers, kills containers that don’t respond to health checks, and clients cannot see containers until they are ready for use. 

Secret and configuration management lets you store and manage sensitive information (i.e., passwords, authentication tokens, and SSH keys). Sensitive information can be updated without rebuilding container images and without exposing secrets in your stack configuration. 
## How it Works
A Kubernetes cluster of nodes is created and then a containerized app is deployed on that cluster(s), creating a network of virtual machines. This containerized app is likely to be docker but does not have to be. 

This aforementioned cluster is created via the command line with command line tools, such as Minikube and Kubectl, which let the user interact with it on either a local level or a widespread level. 

A Kubernetes cluster of nodes is created and then a containerized app is deployed on that cluster(s), creating a network of virtual machines. This containerized app is likely to be docker but does not have to be. 

This aforementioned cluster is created via the command line with command line tools, such as Minikube and Kubectl, which let the user interact with it on either a local level or a widespread level. 

## History
Originally a Google project, much of the Kubernetes team came from the Google Borg team which had a similar goal. Launched in 2014 and currently maintained by the Cloud Native Computing Foundation (CNCF) which was formed in 2015 by Google and the Linux foundation. Kubernetes means “helmsman” in Greek and the seven spoked wheel icon comes from both the name and that Kubernetes was known as “Project 7” internally at Google.  

## Strengths and Weaknesses

| Strengths | Weaknesses |
|-----------|------------|
| Runs in the background | Complicated |
| Allows for easy collaboration across teams | Technical issues|
|Can run across many devices | Long waiting times |
| Utilizes CRI's to spin up containers for use within Kubernetes | Poor User experience |

From what we were able to glean from user comments about Kubernetes, these seem to be the biggest selling points and drawbacks. The most complaints were in regard to the complexity of Kubernetes for new users. The tool is certainly not self explanatory and it can be difficult to understand what is happening without a GUI. As Kubernetes runs in the background, many new users have difficulty visualizing what exactly is happening. 

## Competitors
*Amazon ECS 

*Helios 

*RedHat Open Shift 

*Aptible 

Many of the competitors for Kubernetes are actually managed Kubernetes systems. Their goal is to remove much of the complexity around Kubernetes, making it more accessbile to users without having to have an extensive background in the tool's usage. Some of these competitors include RedHat Open Shift, Spotify's Helios, Amazon ECS, and Aptible.

## An Applied Use Case: Mining Stacks

Stacks is a programmable blockchain built on top of Bitcoin, with similar functionality to Ethereum. While Ethereum uses Proof of Stake mining and Bitcoin uses Proof of Work mining, Stacks uses Proof of Transfer. In practice, Proof of Transfer with Stacks essentially involves spending Bitcoin for the chance to win a block of Stacks tokens. In effect, this mechanism recycles the energy spent by Bitcoin’s proof of work miners. 

In order to mine Testnet Stacks, you must run a testnet Stacks node and a testnet bitcoin node. You also need Docker, minikube, kubectl, and Helm. Helm is essentially a package manager for Kubernetes. By using a Helm chart, life becomes a lot simpler because all the configurations for the Kubernetes cluster are already built in. 

## Our Challenges

Running nodes on Bitcoin and Stacks definitely requires a technical background. For example, settings in the bitcoin node's configuration file initially seemed like gibberish; however, researching and learning about daemon, setting the data directory path and the rest of the customizable settings was very helpful. We did have issues with Stacks documentation and school computer permissions. Thankfully, Professor Sprenkle was an incredible resource as we navigated this uncharted territory. We were able to get both of the nodes running as they should on Marshall's personal computer.

Finally, it was a challenge for us to get a testnet Stacks mining operation fully up and running. We aren’t 100% sure why it wouldn’t work, but we hypothesize that the Helm chart for mining testnet Stacks has not been fully updated along with testnet Stacks updates.

## Helpful Links
### Overview
https://kubernetes.io/docs/concepts/overview/
### Tutorials
Basic Kubernetes tutorials: https://kubernetes.io/docs/tutorials/kubernetes-basics/ 

Includes starting a cluster, deploying an app, exploring your app, exposing your app 	publicly, scaling your app, and updating your app. 
### Documentation
https://kubernetes.io/docs/home/

Minikube: https://cheatsheet.dennyzhang.com/cheatsheet-minikube-a4 

Kubectl: https://kubernetes.io/docs/reference/kubectl/cheatsheet/ 
### Stacks
Run a Testnet Stacks Node: https://docs.stacks.co/understand-stacks/running-testnet-node 

Mine Testnet Stacks: https://docs.stacks.co/start-mining/testnet 

Proof of Transfer: https://docs.stacks.co/understand-stacks/proof-of-transfer

More on Stacks Mining: https://docs.stacks.co/understand-stacks/mining

### Additional
Competitor list: https://www.g2.com/categories/container-orchestration 
