# 🚀 Kubernetes Practice

A personal DevOps project to explore and practice Kubernetes configurations, focusing on deploying and managing a simple Node.js application.

## 📁 Project Structure

```
kubernetes-practice/
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
├── logbook.md
└── readme.md
```

- **k8s/**: Contains Kubernetes manifests for deployment, service, and ingress configurations.
- **logbook.md**: A personal log tracking the learning journey and experiments.
- **readme.md**: Project overview and setup instructions.

## 🛠️ Technologies Used

- **Kubernetes**: Container orchestration platform.
- **Node.js**: Runtime environment for the application.
- **Docker**: Containerization platform.
- **Ingress Controller**: Manages external access to services in the cluster.

## 🚀 Getting Started

### Prerequisites

- Kubernetes cluster (e.g., Minikube, Docker Desktop, or a cloud provider).
- `kubectl` command-line tool configured to interact with your cluster.

### Deployment Steps

1. **Clone the Repository**

   ```bash
   git clone https://github.com/by-sDUDEnt/kubernetes-practice.git
   cd kubernetes-practice
   ```

2. **Apply Kubernetes Manifests**

   ```bash
   kubectl apply -f k8s/
   ```

3. **Verify Deployment**

   ```bash
   kubectl get all
   ```

4. **Access the Application**

   - If using an ingress controller, ensure it's set up correctly.
   - Access the application via the configured ingress host or service IP.



## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
