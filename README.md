# GitHub to On-Premise Kubernetes Deployment Demo

Repository demo để test việc kết nối và deploy từ GitHub đến Kubernetes cluster on-premise.

## 📋 Tổng quan

Repository này bao gồm:
- ✅ Demo web application (Node.js)
- ✅ Dockerfile để containerize application
- ✅ Kubernetes manifests (Deployment, Service, Ingress)
- ✅ GitHub Actions workflow cho CI/CD
- ✅ Hướng dẫn chi tiết setup và deployment

## 🏗️ Kiến trúc

```
GitHub Repository
    ↓
GitHub Actions (CI/CD)
    ↓
Build Docker Image → Push to Container Registry
    ↓
Deploy to On-Premise K8s Cluster
    ↓
Application Running on K8s
```

## 🚀 Quick Start

### 1. Clone repository
```bash
git clone <repository-url>
cd Web-study
```

### 2. Test local
```bash
npm install
npm start
# Truy cập http://localhost:3000
```

### 3. Build và test Docker image
```bash
docker build -t github-k8s-demo:latest .
docker run -p 3000:3000 github-k8s-demo:latest
```

### 4. Deploy lên K8s
```bash
kubectl apply -f k8s/
```

## 📁 Cấu trúc Project

```
.
├── README.md                   # File này
├── app/
│   ├── server.js              # Node.js application
│   └── package.json           # Dependencies
├── Dockerfile                 # Docker image configuration
├── k8s/
│   ├── deployment.yaml        # K8s Deployment
│   ├── service.yaml           # K8s Service
│   └── ingress.yaml           # K8s Ingress (optional)
├── .github/
│   └── workflows/
│       └── deploy.yml         # GitHub Actions workflow
├── scripts/
│   └── deploy.sh              # Deploy script
└── docs/
    └── SETUP_GUIDE.md         # Hướng dẫn setup chi tiết
```

## 🔗 Cách kết nối GitHub với K8s On-Premise

Xem hướng dẫn chi tiết tại: [docs/SETUP_GUIDE.md](docs/SETUP_GUIDE.md)

### Tóm tắt các bước:

1. **Setup Self-Hosted Runner** trên K8s cluster
2. **Configure Secrets** trong GitHub repository
3. **Setup Container Registry** (Docker Hub, Harbor, etc.)
4. **Configure kubectl access** từ GitHub Actions
5. **Deploy using GitHub Actions**

## 🔐 GitHub Secrets cần thiết

Trong repository settings → Secrets and variables → Actions, thêm các secrets:

- `KUBECONFIG`: Content của kubeconfig file
- `DOCKER_USERNAME`: Username của container registry
- `DOCKER_PASSWORD`: Password/token của container registry
- `K8S_NAMESPACE`: Namespace trong K8s cluster (default: default)

## 💻 Tech Stack

- **Application**: Node.js + Express
- **Container**: Docker
- **Orchestration**: Kubernetes
- **CI/CD**: GitHub Actions
- **Registry**: Docker Hub (có thể đổi sang Harbor, GitLab Registry, etc.)

## 📝 License

MIT License

## Test update
