# IAM groups

IAM groups are containers for Users. You cannot log in to a group, they have no credentials.  They are used to make the management of IAM users easier.

Example:

* Group: Developers
  * u/Sally
  * u/Mike

* Group: QA
  * u/Nathalie
  * u/Sally

Groups can have inline or managed policies, and can be combined with the policies that are also on the user within the group.  AWS merges all the policies into a set of permissions on that user.

They is no limit to how many users can be in a group except for the restriction to 5000 users per account.

You cannot have nested groups

Limit of 300 groups per account (can be increased with a support ticket)

**Use case - resource policies:**
You can have a resource policy on a resource (like an S3 bucket). The resource policy on a resource can reference IAM users and IAM roles using an ARN.  

***Groups are not a a true identity, they can't be referenced as a principal in a policy.***

A resource policy cannot grant access to an IAM group.  Groups are just there to group up IAM users and attach IAM policies that members of the group can inherit.