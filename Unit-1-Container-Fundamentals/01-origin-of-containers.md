- Before containers exists, applications were directly deployed on the servers.
- server examples:- linux os, mysql database, java application, python application, nodejs application

# problems with this model

1. Dependency conflicts

- different apps require different versions and libraries.

2. environment Inconsistency

- everyone's machines environment differs from production servers.
  example:-
  Developer Machine:- Python 3.10, Node 18
  Production Server:- Python 3.8, Node 16

3. Poor Resource Isolation

- one application can consume all resources.
  exmpple:-
  App A → Uses 100% CPU
  App B → becomes slow
  App C → crashes

4. Difficult scaling

- if traffic increases, you must manually install the entire stack on another server.
  Install OS
  Install dependencies
  Configure environment
  Deploy application
  , this is slow and error prone

##### virtual machines(first attempt to solve this problem)

-VM architecture
Hardware
│
Hypervisor
│
├── VM1 → OS + App1
├── VM2 → OS + App2
└── VM3 → OS + App3

- Each VM runs a separate os
  Examples of hypervisors:
  VMware
  VirtualBox
  KVM
  Hyper-V

* Advantages of VMs:-

- strong isolation
- separate os environments
- applications can't affect each other

* Problems with VMs:-
  -VMs are very heavy.
  example memory usage:-
  VM1 OS → 1GB RAM
  VM2 OS → 1GB RAM
  VM3 OS → 1GB RAM
  Total wastage RAM:-
  3GB
  Boot time:-
  VM startup = minutes
  Storage:-
  Each VM = full OS

###### Containers:- ##################3
