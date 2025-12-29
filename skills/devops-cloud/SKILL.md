---
name: devops-cloud
description: Master DevOps, cloud infrastructure, containerization, CI/CD, and infrastructure automation. Use when designing deployment strategies, setting up cloud infrastructure, or implementing automation pipelines.
sasmp_version: "1.3.0"
bonded_agent: 01-frontend-ui-specialist
bond_type: PRIMARY_BOND
---

# DevOps & Cloud Infrastructure

## Quick Start

Modern DevOps combines multiple technologies and practices:

```dockerfile
# Dockerfile Example
FROM node:18-alpine

WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production

COPY . .
EXPOSE 3000

HEALTHCHECK --interval=30s --timeout=3s \
  CMD node healthcheck.js

CMD ["node", "server.js"]
```

## Cloud Platforms

### AWS (Amazon Web Services)
- **Compute**: EC2, Lambda, ECS, EKS
- **Storage**: S3, EBS, EFS, Glacier
- **Database**: RDS, DynamoDB, ElastiCache
- **Networking**: VPC, CloudFront, Route 53
- **DevOps**: CodePipeline, CodeDeploy, CloudFormation

### Azure & Google Cloud
- **Azure**: VMs, App Service, AKS, CosmosDB
- **Google Cloud**: Compute Engine, Cloud Run, BigQuery, Cloud Storage

### Infrastructure as Code

#### Terraform
```hcl
resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "web-server"
  }
}

resource "aws_s3_bucket" "data" {
  bucket = "my-data-bucket"

  tags = {
    Name = "Data Storage"
  }
}
```

#### CloudFormation & Ansible
- **CloudFormation**: AWS-native IaC with JSON/YAML
- **Ansible**: Agentless configuration management
- **Puppet/Chef**: Agent-based configuration management

## Containerization

### Docker Fundamentals
- **Images**: Base images, layers, Dockerfile best practices
- **Containers**: Running instances, resource limits
- **Registries**: Docker Hub, ECR, private registries
- **Docker Compose**: Multi-container orchestration locally
- **Optimization**: Layer caching, image size reduction

### Docker Best Practices
```dockerfile
# Multi-stage builds for optimization
FROM node:18 AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build

FROM node:18-alpine
WORKDIR /app
COPY --from=builder /app/dist ./dist
COPY --from=builder /app/package*.json ./
RUN npm ci --only=production

CMD ["node", "dist/server.js"]
```

## Container Orchestration

### Kubernetes (K8s)
- **Clusters**: Nodes, master components, API server
- **Pods**: Basic deployment unit, containers, networking
- **Services**: Load balancing, service discovery (ClusterIP, NodePort, LoadBalancer)
- **Deployments**: Rolling updates, scaling, self-healing
- **StatefulSets**: For stateful applications
- **ConfigMaps & Secrets**: Configuration management

### Kubernetes Resources
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: app
        image: myapp:latest
        ports:
        - containerPort: 3000
        resources:
          limits:
            cpu: 500m
            memory: 512Mi
```

## CI/CD Pipelines

### GitHub Actions
```yaml
name: Deploy
on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '18'
      - run: npm ci
      - run: npm test
      - run: npm run build
      - run: ./deploy.sh
```

### Pipeline Stages
1. **Build**: Compile code, run linters
2. **Test**: Unit tests, integration tests
3. **Security**: SAST, dependency scanning
4. **Package**: Create artifacts, build containers
5. **Deploy**: Staging, production deployment
6. **Monitor**: Health checks, alerting

### Popular CI/CD Tools
- **GitHub Actions**: Native GitHub integration
- **GitLab CI**: Integrated with GitLab
- **Jenkins**: Self-hosted, highly customizable
- **CircleCI**: Cloud-based, developer-friendly

## Monitoring & Observability

### Metrics Collection
- **Prometheus**: Time-series database, metrics scraping
- **Datadog**: Comprehensive monitoring platform
- **Grafana**: Visualization and dashboarding
- **CloudWatch**: AWS native monitoring

### Logging
- **ELK Stack**: Elasticsearch, Logstash, Kibana
- **Splunk**: Centralized logging platform
- **Datadog**: Integrated logging solution
- **Structured Logging**: JSON logs for easy parsing

### Alerting
```yaml
# Prometheus Alert Rules
groups:
- name: alerts
  rules:
  - alert: HighCPU
    expr: cpu_usage > 80
    for: 5m
    annotations:
      summary: "High CPU usage detected"
```

## Linux & Shell Scripting

### Essential Commands
- **File Management**: ls, cp, mv, rm, find
- **Text Processing**: grep, sed, awk, cut
- **System Admin**: systemctl, journalctl, top, htop
- **Networking**: netstat, curl, ssh, scp

### Bash Scripting
```bash
#!/bin/bash
set -euo pipefail

# Check service status
check_service() {
  local service=$1
  if systemctl is-active --quiet $service; then
    echo "$service is running"
  else
    echo "$service is not running"
    exit 1
  fi
}

check_service "nginx"
check_service "docker"
```

## Best Practices

1. **Infrastructure as Code**: Version control all infrastructure
2. **Immutable Infrastructure**: Rebuild instead of modify
3. **Automated Testing**: Test all changes automatically
4. **GitOps**: Version control as source of truth
5. **Security**: Secrets management, scanning, compliance
6. **Scaling**: Horizontal scaling, auto-scaling policies
7. **Disaster Recovery**: Backups, replication, failover

## Learning Resources

- DevOps Roadmap: https://roadmap.sh/devops
- Kubernetes: https://kubernetes.io
- Docker: https://docker.com
- Terraform: https://www.terraform.io
- AWS Training: https://aws.amazon.com/training
