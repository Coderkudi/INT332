# Container Engineering & Docker Notes

This repository contains structured notes and experiments while studying containerization and Docker.

The goal is to understand container technology from the fundamentals, including how containers work internally and how Docker manages them.

## Topics Covered

### Unit 1 – Container Fundamentals

- Origin of Containers
- Emergence of Containerization
- Container Runtime
- Process Isolation
- Linux Namespaces
- Control Groups (cgroups)
- Container Images and Layers
- Image Registries
- Docker Introduction
- Docker Architecture
- Docker Daemon
- Docker CLI
- Docker Objects
- Docker Filesystem

### Unit 2 – Docker Commands

- Container lifecycle
- Running containers
- Executing commands inside containers
- Logs and container inspection

### Unit 3 – Docker Images

- Dockerfile
- Image building
- Image layering
- Image optimization

### Unit 4 – Docker Networking

- Bridge networks
- Host networking
- Container communication

### Unit 5 – Docker Storage

- Volumes
- Bind mounts
- Storage drivers

### Unit 6 – Container Orchestration

- Docker Compose
- Introduction to Kubernetes
- Container scaling

## Experiments

The repository also contains practical experiments performed using Docker on Linux to understand container behavior and architecture.

-------------****************\*\*\*\*****************----------------------

container-engineering
│
├── README.md
│
├── Unit-1-Container-Fundamentals
│ ├── 01-origin-of-containers.md
│ ├── 02-emergence-of-containerization.md
│ ├── 03-container-runtime.md
│ ├── 04-process-isolation.md
│ ├── 05-linux-namespaces.md
│ ├── 06-cgroups.md
│ ├── 07-container-images.md
│ ├── 08-image-registries.md
│ ├── 09-docker-introduction.md
│ ├── 10-docker-architecture.md
│ ├── 11-docker-daemon.md
│ ├── 12-docker-cli.md
│ ├── 13-docker-objects.md
│ └── 14-docker-filesystem.md
│
├── Unit-2-Docker-Commands
│ ├── container-lifecycle.md
│ ├── docker-run.md
│ ├── docker-exec.md
│ ├── docker-logs.md
│ ├── docker-inspect.md
│ └── docker-stats.md
│
├── Unit-3-Docker-Images
│ ├── dockerfile-basics.md
│ ├── docker-build.md
│ ├── docker-image-layers.md
│ └── image-optimization.md
│
├── Unit-4-Docker-Networking
│ ├── bridge-network.md
│ ├── host-network.md
│ ├── overlay-network.md
│ └── container-communication.md
│
├── Unit-5-Docker-Storage
│ ├── volumes.md
│ ├── bind-mounts.md
│ └── storage-drivers.md
│
├── Unit-6-Container-Orchestration
│ ├── docker-compose.md
│ ├── introduction-to-kubernetes.md
│ └── container-scaling.md
│
└── experiments
├── namespace-experiment.md
├── container-process-test.md
├── image-layer-test.md
└── docker-network-test.md
