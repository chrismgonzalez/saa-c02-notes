# IAM roles

IAM roles are best suited for more than one identity that needs temporary access to an AWS resource.

Roles are generally used on a temporary basis and represent a level of access that you can have for a short period of time.

Essentially, the IAM user will borrow the permissions associated with an IAM role for a short period of time. A role represents a level of access within an AWS account.

IAM roles have 2 types of policies that can be attached.

1. **Trust policy** - the trust policy controls which identities can assume the role.  The trust policy can reference identities in the same account and also other accounts.
   1. If a role gets assumed by a role that allowed to assume it (using the trust policy), then AWS generates temporary security credentials.
   2. These are made available to the identity that assumed the role and are time limited.
   3. The temporary credentials will allow the identity access to the resources listed in the permissions policy of the role.
2. **Permissions policy** - list of permissions that the identity assuming the role can have on a resource.

Roles are used within an organization to access resources in other accounts within the organization.

When you assume a role, temporary controls are generated for a user using STS, security token serivce. Syntax of the operation: **sts.AssumeRole**

## When to use IAM roles

- AWS services operate on your behalf and need access rights to perform actions.
- When you need emergency access to resources (break glass), using an emergency role.
- When you are integreting AWS into existing infrastructure, integrating with Microsoft Active Directory (SSO sign-on)
- Designing a mobile application that needs to interact with AWS resources to retrive data.
  - Use a web identity tht assumes a role within AWS to retrieve the data.  (ID Federation)
