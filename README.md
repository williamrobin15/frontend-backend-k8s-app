# Frontend-Backend Kubernetes App

This repository contains a simple **frontend and backend application** deployed on **Kubernetes** using YAML manifests.
It demonstrates how to run and connect multi-service applications on Kubernetes with scaling and persistence.

---

## 📂 Project Structure

```
.
├── backend-manifest/
│   ├── helloworld-backend-deployment.yaml   # Backend Deployment
│   ├── hellowolrd-backend-service.yaml      # Backend Service
│   ├── helloworld-backend-hpa.yaml          # Horizontal Pod Autoscaler
│   ├── helloworld-backend-pv.yaml           # Persistent Volume
│   ├── helloworld-backend-pvc.yaml          # Persistent Volume Claim
│
├── frontend-manifest/
│   ├── helloworld-frontend-deployment.yaml  # Frontend Deployment
│   ├── helloworld-frontend-service.yaml     # Frontend Service
│   ├── helloworld-frontend-hpa.yaml         # Horizontal Pod Autoscaler
```

---

## 🚀 Features

* **Frontend & Backend** microservices
* Kubernetes **Deployment** & **Service**
* **Horizontal Pod Autoscaler (HPA)** for auto-scaling
* **Persistent Volume & PVC** for backend storage
* Easy to extend with Ingress/LoadBalancer

---

## 🛠️ Prerequisites

* Kubernetes Cluster (Minikube, Kind, GKE, EKS, or AKS)
* `kubectl` installed and configured
* gcr must be setup with hello world image
* Docker (if you need to build custom images)

---

## 📦 Deployment

1. Clone the repository:

   ```bash
   git clone https://github.com/williamrobin15/frontend-backend-k8s-app.git
   cd frontend-backend-k8s-app
   ```

2. Apply backend manifests:

   ```bash
   kubectl apply -f backend-manifest/
   ```

3. Apply frontend manifests:

   ```bash
   kubectl apply -f frontend-manifest/
   ```

4. Verify resources:

   ```bash
   kubectl get pods
   kubectl get svc
   kubectl get hpa
   ```

---

## 🌐 Access the Application

* Get the **frontend service** URL:

  ```bash
  kubectl get svc helloworld-frontend-service
  ```
* Open the given **NodePort / LoadBalancer IP** in your browser.
* Frontend will internally call the backend service.

---

## 📖 Learning Outcomes

* Deploying **multi-service apps** on Kubernetes
* Using **HPA** for auto-scaling
* Attaching **Persistent Volumes** to workloads
* Organizing manifests for clean deployments

---

