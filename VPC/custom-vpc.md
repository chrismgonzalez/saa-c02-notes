# Custom VPCs

## Concepts to understand

* Regional Service - all AZs in the region
* Isolated network
* Nothing IN or OUT without explicit configuration
* Flexible configuration - simple or multi-tier
* Hybrid Networking - other cloud & on-premises
* Default or Dedicated Tenency
* IPv4 Private CIDR blocks & public IPs
* 1 primary Private IPv4 CIDR block
* Min /28 (16 IP) to max /16 (65,536 IP)
* Optional secondary IPv4 Blocks
* Optional single assigned IPv6 /56 CIDR block

## DNS in a VPC

* Provided by R53
* VPC Base IP + 2 address
* enableDnsHostnames - gives instances DNS names
* enableDnsSupport - enables DNS resolution in a VPC
