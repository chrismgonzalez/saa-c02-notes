# IAM Users & ARNs

IAM Users are one of the identity types available inside AWS.

IAM Users are an identity used for anything requiring **long-term** AWS access e.g. **Humans**, **Applications**, or **service accounts**.

They are type you pick when you can identity a single individual or 'thing' which will use that identity - a person, an application, or a service account.

## Authentication & Authorization Architecture

---

IAM users start as a **Principal** (can be a user, a computer, services) that make a request to IAM. During the process of authentication with IAM, it must prove who it is it claims to be. The Principal authenticates via username/password or access keys.

Once a Principal has authenticated, it is now an authenticated identity.  **Authentication** is the method by which a principal proves itself, either by username/password or access key.  **Authorization** is then the act of checking the policies that are applicable to the user and subsequently allowing or denying access to AWS resources.

## Amazon Resource Name (ARN)

---
ARNs uniquely identify resources within any AWS accounts.

ARNs are a collections of fields separated by a colon. If nothing exists between colons then that field does not need to be specified.  A wildcard can also be used. Use a wildcard when you want to refer to a wildcard collection of things.  Not all ARNs need all fields (like S3 buckets that have a globally unique name.)

Format:

```sh
  arn:partition:service:region:account-id:resource-id
  arn:partition:service:region:account-id:resource-type/resource-id
  arn:partition:service:region:account-id:resource-type:resource-id
```

Example:

```sh
# these arns are different and DO NOT overlap

# refers to a bucket
arn:aws:s3:::catgifs
# refers to objects in a bucket
arn:aws:s3:::catgifs/*
```

Obscurities:

* 5000 IAM users **per account**
* IAM User can be a member of 10 groups
