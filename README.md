# docker-compose-files

A collection of production-ready Docker Compose configurations for common services used in DevOps workflows.

## Contents

| File | Service | Description |
|---|---|---|
| `docker-compose for jenkins` | Jenkins | Jenkins CI server with persistent volume |
| `docker-compose for sonarqube` | SonarQube | Code quality and security scanner |
| `docker-compose for MYSQL` | MySQL | MySQL database with persistent storage |
| `docker-compose for PSQL` | PostgreSQL | PostgreSQL database with persistent storage |
| `docker-compose for SQL` | SQL Server | Microsoft SQL Server container |
| `docker-compose for oracle` | Oracle DB | Oracle database container |
| `Dockerfile-Angular` | Angular | Multi-stage build for Angular apps |
| `Dockerfile-Python` | Python | Production Dockerfile for Python apps |

## Usage

```bash
# Clone the repo
git clone https://github.com/Vishal-B142/docker-compose-files.git
cd docker-compose-files

# Start any service
docker compose -f "docker-compose for jenkins" up -d
```

## Prerequisites

- Docker 20.10+
- Docker Compose v2+

## Notes

- All compose files use named volumes for data persistence
- Jenkins compose exposes port `8080` (UI) and `50000` (agents)
- SonarQube requires at least 2GB RAM — set `vm.max_map_count=262144` on the host
- Database compose files include health checks for readiness probing

## Related

- [jenkins-k8s-pipeline](https://github.com/Vishal-B142/jenkins-k8s-pipeline) — CI/CD pipeline using Jenkins and Kubernetes
- [observability-stack](https://github.com/Vishal-B142/observability-stack) — Prometheus + Grafana monitoring stack
