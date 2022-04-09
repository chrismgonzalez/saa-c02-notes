# AWS Global Infrastructure

The AWS Global Network contains two types of deployments: AWS Regions & AWS Edge Locations.

## Regions

---

AWS regions are located throughout the world.  They provide full compute, db, ai, and many other services.
Regions are fault-tolerant by design due to their geographic separation.  They also provide geopolitical separation.  If you house your cloud assets in the EU, for example, you are bound by the local laws and governance of that region (think GDPR). Regions also allow for location control which increases performance.

### Breakdown of a region (Regions and AZs)

Region Code, name: us-east-1, Northern Virginia

Inside the us-east-1 region we have 3 availability zones: us-east-1a, 1b, 1c

AZs are fully independent with their own power, cooling, and security.

## Edge Locations

---
AWS Edge Locations provide the capability to store data in edge locations close to customers for use cases like data streaming and caching.  AWS edge locations are local distribution points.

## Resiliency

---
**Globally Resilient** - can tolerate outages across multiple regions (examples: IAM, Route53)

**Region Resilient** - operate in a single region, they operate as separate service in each region but replicate their data across AZs

**AZ Resilient** - services that are run in a specific AZ.  If the AZ has an outage, that service will be unavailable.
