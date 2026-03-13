# Container Runtime

## Definition

A container runtime is software responsible for running containers on a host system.

It creates the container environment and starts the container process using Linux kernel features such as namespaces and control groups.

---

## Role of Container Runtime

Container runtime performs the following tasks:

- Create container environment
- Configure namespaces for isolation
- Apply cgroups for resource limits
- Setup container filesystem
- Start the container process

Without a runtime, a container image cannot be executed.

---

## Container Execution Flow

When a container is started using Docker, the following components are involved:

Docker CLI
↓
Docker Daemon
↓
containerd
↓
runc
↓
Linux Kernel

The runtime ultimately interacts with the Linux kernel to start the container process.

---

## Types of Container Runtimes

### Low-Level Runtime

Low-level runtimes directly interact with the Linux kernel to create containers.

Example:

runc

Responsibilities:

- Create namespaces
- Apply cgroups
- Setup filesystem
- Launch container process

---

### High-Level Runtime

High-level runtimes manage container lifecycle and interact with low-level runtimes.

Examples:

- containerd
- CRI-O

Responsibilities:

- Manage container images
- Start and stop containers
- Manage container storage
- Communicate with low-level runtime

---

## runc

runc is the reference container runtime that follows OCI standards.

It is responsible for actually creating and running containers.

Docker ultimately uses runc to launch container processes.

---

## containerd

containerd is a high-level container runtime used by Docker and Kubernetes.

It manages container lifecycle and communicates with runc to run containers.

---

## Open Container Initiative (OCI)

OCI defines standards for container runtimes and container images.

These standards ensure that containers can run across different platforms and tools.

Examples of platforms supporting OCI standards include Docker, Podman, and Kubernetes.

---

## Summary

A container runtime is responsible for executing containers by interacting with the Linux kernel.

The runtime creates isolated environments using namespaces and resource limits using cgroups.

Popular runtimes include runc and containerd.
