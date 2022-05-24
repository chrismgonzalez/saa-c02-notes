# S3 Security (Resource Policies and ACLs)

S3 is private by default, the only identity that has access to the S3 bucket by default is the account root user of the account that created the S3 bucket.

You can grant access to the S3 bucket by applying the following security measures:

* Apply a **bucket policy**, which is a type of resource policy.
  * Resource policies are like an identity policy, but for resources
  * They are resource perspective permissions
  * They apply only to resources within your account.
  * Resource policies are a great way of controlling access to resources inside your account
  * ALLOW/DENY identities in the same or different accounts.
  * ALLOW/DENY anonymous principals (any user)

Example bucket policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3:::secretcatproject/*"]
    }
  ]
}
```

More bucket policy examples can be found [here](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html)

## Access Control Lists

* ACLs are legacy and AWS prefers that you use bucket policies
* ACLs are very general when it comes to ACLs
* NEVER use them - unless you must

## Block Public Access

* You can block all public access to public or anonymous identities.

## Recap

When to use certain types of policies...

* Identity: Controlling different resources
* Identity: You have a preference for IAM
* Identity: Same account
* Bucket: Just controlling S3
* Bucket: Anonymous or Cross-Account
* ACLs: Never - unless you must
