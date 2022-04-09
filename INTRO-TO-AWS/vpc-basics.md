# Virtual Private Cloud (Basics)

A VPC is a virtual network inside AWS.  They are regional services, which means they are regionally resilient.  By default it is private and isolated.  Services within it can communicate with other services inside the same VPC.  VPCs cannot communicate with each other without additional configuration.

* Two types - Default VPC and Custom VPCs
  * Custom VPCs can be configured exactly how you need.  By default, they are completely private.
  * Default VPCs are configured by AWS, and only 1 exists per region.
    * Has a default CIDR of 172.31.0.0/16
    * It has 3 subnets, one inside each AZ within a region.
    * One per region - can be removed and recreated as needed (don't use it)
    * A /20 subnet is placed in each AZ in the region
    * An Internet Gateway (IGW), Security Group (SG) & NACL are also created.
    * Subnets assign public IPv4 addresses

Default VPC example subnet:

SN-A: 172.31.0.0/20; Start: 172.31.0.0, End: 172.31.15.255

SN-A: 172.31.16.0/20; Start: 172.31.16.0, End: 172.31.31.255

SN-A: 172.31.32.0/20; Start: 172.31.17.0, End: 172.31.32.255
