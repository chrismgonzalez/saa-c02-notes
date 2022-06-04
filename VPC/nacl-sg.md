# NACLs and Security Groups

## Network Access Control List (NACL)

A network access control list (NACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.

## Important NACL concepts

* Stateless - Request and response seen as different
* Only impacts data crossing subnet boundary
* NACLs can explicitly allow and deny
* IPs/CIDR, Ports & protocols - no logical resources
* NACLs cannot be assiged to AWS resources - only subnets
* Use together with Security groups to add explicit deny (bad IPs/Nets)
* Each subnet can have one NACL (default or custom)
* An NACL can be associated with many subnets

Example:

![image nacl](/VPC/visual-aides/nacl.png)

---

## Security groups

Security Groups (SGs) are another security feature of AWS VPC ... only unlike NACLs they are attached to AWS resources, not VPC subnets.

SGs offer a few advantages vs NACLs in that they can recognize AWS resources and filter based on them, they can reference other SGs and also themselves.

But.. SGs are not capable of explicitly blocking traffic - so often require assistance from NACLs

## Important SG concepts

* Stateful - detect response traffic automatically
* Allowed (IN or OUT) request = allowed response
* No explicit deny - only allow or implicit deny
* Cant block specific bad actors
* Supports IP/CIDR and logical resources including other security groups and itself
* Attached to ENI (Elastic Network Interface) not instances

### Security group overview visual

![image sg](/VPC/visual-aides/sg.png)

### Security group logical resource

![image sg-logical](/VPC/visual-aides/sg.png)

### Security group self-reference

![image sg-self-ref](/VPC/visual-aides/sg.png)
