# EC2 Architecture and Resilience

## Architecture

- AZ Resilient service
  - If the AZ where the host is located fails, the instance will be unavailable
- Are Virtual machines
- Instances run on EC2 hosts
  - Instances are locked to an availability zone
- Shared hosts and dedicated hosts

- Can access remote storage in the same AZ - EBS
- EBS cannot be accessed across AZs, it is isolated to a specific AZ

## What is it good for?

- Traditional OS + Application compute requirements
- Long-running compute
- Server style applications
- either burst or steady-state load
- Monolithic application stacks
- Migrating application workloads or Disaster Recovery
- It is the default, traditional compute workload handler
