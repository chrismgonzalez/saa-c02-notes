# CloudTrail Essentials

Almost everything that can be done in an AWS account is logged by CloudTrail. CloudTrail is a regional service, but can be configured to collect trails from all regions.

It's very often used to diagnose security or performance issues, or to provide quality account level traceability.

It can be configured to store data indefinitely in S3 or CloudWatch Logs.

* Logs API calls/activities as a **CloudTrail Event**
* 90 days of history stored by default in **Event History**
* To customize the service you can create 1 or more *Trails*
* Management Events are logged by default and Data events can be logged for an additional cost.
* Global services like IAM, STS, CloudFront generate global service event - need to configure to send to USE-1
* Events do not arrive to the destination in real time, there is a delay.
