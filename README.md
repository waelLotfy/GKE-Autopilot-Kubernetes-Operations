# GKE-Autopilot-Kubernetes-Operations
Hands‑on deployment and management of a Google Kubernetes Engine (GKE) Autopilot cluster, including workload deployment, Pod introspection, networking, and observability using kubectl and Cloud Shell.

# GKE Autopilot Cluster Deployment and Kubernetes Operations

This project demonstrates how to deploy and operate a **Google Kubernetes Engine (GKE) Autopilot cluster** using **Cloud Shell**, manage Kubernetes workloads with `kubectl`, and inspect Pods, services, logs, and resource usage.

The lab focuses on real‑world Kubernetes operations using Google‑managed infrastructure.

---

## 🛠 Technologies Used

- Google Kubernetes Engine (GKE)
- GKE Autopilot mode
- Kubernetes
- kubectl
- Google Cloud Shell
- NGINX container image

---

## 📐 Key Concepts Covered

- GKE Autopilot cluster provisioning
- Kubernetes authentication and kubeconfig
- kubectl configuration and contexts
- Pod and Deployment management
- Resource monitoring and autoscaling
- Service exposure and networking
- Pod introspection and debugging
- YAML‑based Kubernetes manifests

---

## 🚀 Implementation Overview

### 1️⃣ Deploying a GKE Autopilot Cluster

- Created a **regional GKE Autopilot cluster** using Cloud Shell
- Used the `gcloud container clusters create-auto` command
- Cluster deployed in the `us-west1` region
- Leveraged Google‑managed defaults for nodes, scaling, security, and upgrades

**Cluster Name:** `autopilot-cluster-1`  
**Mode:** Autopilot  
**Region:** `us-west1`

Autopilot mode abstracts node management and applies production‑ready best practices automatically.

---

### 2️⃣ Connecting to the Cluster and Configuring kubectl

- Retrieved cluster credentials using: gcloud container clusters get-credentials

- Inspected the kubeconfig file stored in `~/.kube/config`
- Verified active context and cluster connectivity
- Enabled kubectl bash autocompletion for improved CLI productivity

---

### 3️⃣ Inspecting the Cluster with kubectl

- Viewed cluster information and control plane endpoints
- Listed available contexts and switched contexts when needed
- Verified Kubernetes system services and metrics availability

---

### 4️⃣ Deploying and Managing Pods

- Deployed an NGINX application using a Kubernetes Deployment
- Verified Pod creation and status
- Inspected Pod details including:
- resource requests and limits
- scheduling events
- QoS class
- node assignment
- Monitored resource usage using:kubectl top nodes, kubectl top pods

- 
---

### 5️⃣ Exposing the Application

- Created a LoadBalancer Service to expose the Pod externally
- Retrieved the external IP address
- Verified application access using `curl` and a web browser

---

### 6️⃣ Pod Introspection and Debugging

- Deployed a Pod using a YAML manifest
- Connected to a running container using: kubectl exec -it
- Installed tools inside the container for troubleshooting
- Modified container content at runtime
- Used port forwarding to access the Pod locally
- Viewed and streamed Pod logs with timestamps

---

## 🧠 Key Learnings

- How GKE Autopilot simplifies Kubernetes infrastructure management
- How kubectl communicates with the Kubernetes control plane
- Understanding Pods, Deployments, and Services in practice
- Kubernetes scheduling, autoscaling, and resource management
- Working with Kubernetes YAML manifests

---

## 📎 Notes

This project was completed as part of the **Google Cloud Skills Boost** Kubernetes learning path and demonstrates production‑oriented Kubernetes operations using GKE Autopilot.
