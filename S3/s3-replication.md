# S3 Replication

S3 has to replication features which allow objects to be replicated between a SOURCE and DESTINATION buckets in the same or different AWS accounts.

Cross-Region Replication (CRR) is the process used when Source and Destination are in different AWS regions

Same-Region Replication (SRR) is used when the buckets are in the same region.

When replicating to a different AWS account, you'll need a cross account role that contains the permissions and trust to assume roles in other accounts.  You need a bucket policy in the destination account that allows the role in the source account to add objects to it.

What to replicate:

* All objects or a subset of objects
* Storage class - default is to maintain the same storage class.
* Ownership - default is the source account
  * different accounts - still owned by the source account, but can be set to be owned by destination account.
* Replication Time Control (RTC)

Considerations:

* Not retroactive & Versioning needs to be ON
* One-way replication Source to Destination
* Unencrypted, SSE-S3 & SSE-KMS (with extra config)
* Source bucket owner needs permissions to objects
* No system events, Glacier or Glacier Deep Archive

Why use replication?

* SRR - Log Aggregation
* SRR - PROD and TEST sync
* SSR - Resilience with strict sovereignty
* CRR - Global Resilience Improvements
* CRR - Latency Reduction
