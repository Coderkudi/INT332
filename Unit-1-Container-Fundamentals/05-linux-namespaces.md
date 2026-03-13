# Linux Namespaces

## Definition

Linux namespaces are a kernel feature that provides isolation of system resources between processes.

Namespaces allow processes to have their own view of system resources such as processes, network interfaces, hostnames, and filesystems.

They are one of the fundamental technologies used to implement containers.

---

## Purpose of Namespaces

Without namespaces, all processes on a system would share the same global resources.

Namespaces isolate these resources so that processes running inside containers appear to run on separate systems.

---

## Types of Linux Namespaces

Linux supports several namespace types.

| Namespace | Description                                  |
| --------- | -------------------------------------------- |
| PID       | Isolates process IDs                         |
| NET       | Isolates network interfaces and IP addresses |
| MNT       | Isolates filesystem mount points             |
| UTS       | Isolates hostname and domain name            |
| IPC       | Isolates interprocess communication          |
| USER      | Isolates user and group IDs                  |

---

## PID Namespace

The PID namespace isolates process IDs.

Each container has its own process tree.

Example inside container:

PID 1 → application process
PID 5 → worker process

These processes cannot see processes running in other containers.

---

## Network Namespace

The network namespace provides each container with its own network stack.

Each container gets:

- its own IP address
- network interfaces
- routing table
- port space

This allows multiple containers to use the same ports internally.

---

## Mount Namespace

The mount namespace isolates filesystem mounts.

Containers see their own filesystem environment derived from container images.

This prevents containers from accessing the host filesystem directly.

---

## UTS Namespace

UTS namespace isolates system identifiers such as hostname and domain name.

Containers can have different hostnames from the host machine.

---

## IPC Namespace

IPC namespace isolates interprocess communication mechanisms such as shared memory and message queues.

Processes in different containers cannot communicate through these IPC mechanisms.

---

## User Namespace

User namespace isolates user and group IDs.

A user inside a container may appear as root but may map to a non-root user on the host system.

This improves container security.

---

## Role of Namespaces in Containers

Container runtimes create namespaces when starting containers.

Namespaces provide isolation for processes, networking, filesystem, and other system resources.

This isolation makes containers behave like independent systems while sharing the same Linux kernel.
