# Elastic Compute Cloud (EC2) basics

EC2 provides access to AWS compute resources that require some sort of server.  EC2 provides virtual machines, called instances.  It runs in the private AWS zone and uses VPC networking.  Allowing public access must be configured through security groups that open up ports and IPs to the public internet.  It is AZ resilient: the instance fails if the AZ fails.

EC2 is Iaas, which means you manage the OS upwards in the stack.  You only pay for what you consume, such as CPU, storage, memory, etc.

Storage can be hosted locally on the instance or from EBS (Elastic Block Store)

## Instance lifecycle

---

**Running** - can move to stopped to shut off the instance

**Stopped** - can be started again, changes state to "running"

**Terminated** - terminate the instance (cannot be turned back on, essentially deleted).

While the instance is running you are charged for resources being consumed (network, memory, cpu).  You are not charged when the instance is stopped.

EBS storage charges are still incurred if the instance is stopped.

## AMI (Amazon Machine Image)

---

A pre-built or custom image that serves as the OS/Permissions for the EC2 instance.  Can be public or custom permissions (implicit allow or explicit allow).

Contains the root volume that boots the instance.  Also contains a block device mapping which is a map of volumes attached to the instance.

## Connecting to EC2

---
Uses RDP (port 3389) on Windows and SSH (port 22) on Mac/Linux.

EC2 uses ssh key pair to authenticate.  You keep the private key on your machine, and the instance holds the public key.
