# IAM Policies

IAM policy documents are simply JSON files made up of 1 or more **statements**.

A statement is a way to tell IAM what access you want to grant to an **identity**

Identity Policies are attached to AWS identities and either ALLOW or DENY access to AWS resources.

## Priorities

* **Explicit DENY** - this operation always takes priority over all other operations
* **Explicit ALLOW** - you have access unless there is an explicit DENY

DENY -- ALLOW -- DENY

## Types of Policies

---

* **Inline policies**
  * These policies are attached to each user/resource
  * Hard to manage
  * Used for exceptions to normal access rights
    * Blocking or allowing permissions for a specific user

* **Managed Policies**
  * Reusable policies
  * Low management overheard
  * Use for common sets of policies in an organization

### Example Policy Document

---

```json
{
    "Version": "2012-10-17",
    "Statement": {
      {
        "Sid": "FullAccess",
        "Effect": "Allow",
        "Action": ["s3:*"],
        "Resource": ["*"]
      },
      {
        "Sid": "DenyCatBucket",
        "Action": ["s3:*"],
        "Effect": "Deny",
        "Resource": ["arn:aws:s3:::catgifs", "arn.aws.s3:::catgifs/*"]
      }
    }
}
```
