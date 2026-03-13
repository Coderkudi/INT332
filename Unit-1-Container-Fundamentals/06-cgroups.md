# cgroups

- cgroups are

* namespaces isolate, cgroups control.

a company uses containers for microservices. one faulty container crashes the host due to high memory usage.
which container feature was misconfigured or missing? cgroups
which kernel mechanism should have prevented this? cgroups
would namespaces alone solve this issue?why?

a server is running three containers.
container A runs a cpu-intensive task
container B runs a web server
container C runs a database

which linux feature prevents container A from consuming all CPU?
which feature ensures container B cannot see processes of container C?
which namespace allows all three containers to use port 80 internally?

---

#########****\*\*****\*\*\*\*****\*\*****\*****\*\*****\*\*\*\*****\*\*****#####

# Control Groups (cgroups)

## Definition

Control Groups (cgroups) are a Linux kernel feature used to limit, control, and monitor the resource usage of processes.

They allow the operating system to allocate resources such as CPU, memory, disk I/O, and network bandwidth to groups of processes.

cgroups are a fundamental technology used in container systems to prevent resource abuse.

---

## Purpose of cgroups

When multiple applications or containers run on the same system, they compete for system resources.

Without resource control, one process could consume excessive CPU or memory and negatively affect other processes.

cgroups solve this problem by enforcing resource limits.

---

## Resources Managed by cgroups

cgroups can control the following system resources:

| Resource | Description                         |
| -------- | ----------------------------------- |
| CPU      | Limits processor usage              |
| Memory   | Limits RAM usage                    |
| Disk I/O | Controls disk read/write operations |
| Network  | Controls network bandwidth          |
| PIDs     | Limits number of processes          |

---

## CPU Control

cgroups allow the operating system to allocate CPU resources to different process groups.

Example Docker command:

docker run --cpus="1.5" myapp

This limits the container to using a maximum of 1.5 CPU cores.

---

## Memory Control

Memory usage can be restricted using cgroups.

Example:

docker run -m 512m nginx

This limits the container to 512 MB of RAM.

If the container exceeds this limit, the Linux kernel may terminate the process.

---

## Disk I/O Control

cgroups can control disk read and write speeds to prevent heavy workloads from blocking storage access for other processes.

---

## Process Limits

The PID controller can restrict the number of processes that a container can create.

This prevents runaway programs or fork bombs from affecting the system.

---

## cgroup Hierarchy

Processes are organized into hierarchical groups called control groups.

Each group can have specific resource limits applied to it.

---

## cgroups in Linux

Linux exposes cgroups through the filesystem:

/sys/fs/cgroup/

Configuration files in this directory define limits for CPU, memory, and other resources.

---

## Role of cgroups in Containers

Container runtimes use cgroups to enforce resource limits for containers.

For example, Docker uses cgroups to control CPU and memory usage of containers.

This ensures that no container can monopolize system resources.
