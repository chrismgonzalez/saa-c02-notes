# AWS Public & Private Services

Public services in AWS are those which you can access over the public internet, like S3.

Private services are those which you can only access from within a VPC.

When thinking about public and private "zones", one can conceptualize that the "public internet" zone would be like having direct access to internet services like Gmail, Netflix, and YouTube.  Whereas private zones would be something like a home network.  Nothing can access a private zone unless you configure it.

In a private zone, only devices that you configure to allow access to the public internet can reach the public internet.

Within AWS, we have the VPC. The VPC, Virtual Private Cloud, is isolated unless configured otherwise.  It is in the "AWS Private Zone".

AWS also has a "public zone."  Public zone AWS services are services that operate with public endpoints, like S3.
