# VPC Subnets

## Concepts to understand

* AZ resilient
* A subnetwprk of a VPC - within a particular AZ
* 1 subnet => 1 AZ, 1 AZ => 0+ subnets
* IPv4 CIDR is a subset of the VPC CIDR
* Cannot overlap with other subnets
* Optional IPv6 CIDR (/64 subset of the /56 VPC - space for 256)
* Subnets can communicate with other subnets in the VPC

## Subnet IP addressing

* Reserved IP addresses (5 in total)
* 10.16.16.0/20 (10.16.16.0 => 10.16.31.255)
* Network address (10.16.16.0)
* "Network +1" (10.16.16.1) - VPC router
* "Network +2" (10.16.16.2) - Reserved (DNS*)
* "Network +3" (10.16.16.3) - Reserved future use
* Broadcast address 10.16.31.255 (Last IP in subnet)
