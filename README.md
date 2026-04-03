# K8s Nginx Deployment using Minikube

## Tools Used
- Minikube (Local Kubernetes Cluster)
- Kubectl
- Nginx

## Project Structure
```
k8s-nginx-task/
├── deployment.yaml   # Nginx Deployment with 2 replicas
├── service.yaml      # NodePort Service to expose Nginx
└── README.md         # Project documentation
```

## Steps to Run

### 1. Start Minikube
```bash
minikube start
```

### 2. Apply Deployment
```bash
kubectl apply -f deployment.yaml
```

### 3. Apply Service
```bash
kubectl apply -f service.yaml
```

### 4. Verify Running Pods
```bash
kubectl get nodes
kubectl get pods
kubectl get svc
kubectl get deployment
```

### 5. Access Application
```bash
minikube service nginx-service --url
```
Open the URL in your browser — you will see the Nginx Welcome Page.

## Tech Stack
- AWS EKS (simulated locally using Minikube)
- EKSCtl equivalent: Minikube
- Kubectl

## Output
- Nginx is accessible outside the cluster via NodePort 30080
- 2 replicas running successfully
