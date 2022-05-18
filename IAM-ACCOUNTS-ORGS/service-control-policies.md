# Service Control Policies (SCPs)

Service control policies are a feature of AWS organizations which allow restrictions to be placed on MEMBER accounts in the form of boundaries.

SCPs can be applied to the organization, to OU's or to individual accounts.

Member accounts can be effected, the MANAGEMENT account cannot.

SCPs DON'T GIVE permission - the just control what an account CAN and CANNOT grant via identity policies.

SCPs do not apply to the management account within an org, so it is best to not let the management account handle any resources.

SCPs are policy documents in JSON format that can be attached to OUs, member organizations, organizations that are chilren of organizations.  When attached at the management level, they are cascaded to all levels underneath.

SCPs:

- are account permissions boundaries
- they limit what the account ( including account root user) can do
- They **don't grant** any permissions

SCPs can have allow lists and deny lists, just like IAM policies they are be default a Deny lists.  Remember, explicit deny takes precedence over other permissions.

A deny list architecture is much lower admin overhead.

Effective permissions for identities in an account are the overlap of Identity policies in accounts and any applicable SCPs.

Example SCP lists:

```json
// below is an example of an explicit allow list
{
  "Version": "2021-10-17",
  "Statement": [
    {
        "Effect": "Allow",
        "Action": "*",
        "Resource": "*"
    }
  ]
}
```

---

```json
// below is an example of a DenyS3 list
{
  "Version": "2021-10-17",
  "Statement": [
    {
        "Effect": "Deny",
        "Action": "s3:*",
        "Resource": "*"
    }
  ]
}
```

---

```json
// below is an example of explicit allow for S3 and EC2
{
  "Version": "2021-10-17",
  "Statement": [
    {
        "Effect": "Allow",
        "Action": [
          "s3:*",
          "ec2:*"
          ],
        "Resource": "*"
    }
  ]
}
```
