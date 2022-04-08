# Cloud

## Five Characteristics of the Cloud

1. **On-Demand Self-Service**

    * can provision capabilities as needed without requiring human interaction.

2. **Broad Network Access**

    * Capabilities are available over the network and accessed through standard mechanisms.

3. **Resource Polling**

    * There is a sense of location independence...no control or knowledge over the exact location of the resources.

    * Reources are pooled to serve multiple consumers using a multi-tenant model.

4. **Rapid Elasticity**
  
    * Capabilities can be elastically provisioned and released to scale rapidly outward and inward with demand.

    * To the consumer, the capabilities available for provisioning often appear to be unlimited.

5. **Measured service**

    * Resources usage can be monitored, controlled, reported...AND billed.

## Types of Cloud (Public, Private, Hybrid, Multi-cloud)

* **Public Cloud**: The meet the five characteristics of cloud and are freely available to the public
* **Multi-cloud**: Using more than one public cloud for your apps (GCP & AWS, AWS & Azure, or any combination of the cloud providers)
* **Private Cloud**: On-premises cloud infrastructure
  * AWS Outposts
  * Azure Stack
  * Google Anthos
* **Hybrid Cloud**: Public Cloud and Private Cloud at the same time, part of your resources are on-prem, other parts are in the public cloud.

## Cloud Service Models

* **Infrastructure as a Service (IaaS)**
  * The Vendor manages the facilities, infrastrucutre, servers, and virtualization.
  * The user consumes the O/S upward
* **Platform as a Service (PaaS)**
  * The vendor manages the facilities, infrastrucutre, servers, virtualization, OS, and container.
  * The user consumes the runtime upward.
* **Software as a Service (SaaS)**
  * Vendor manages all parts of the stack
  * The user consumes the application.
