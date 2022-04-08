# IAM

IAM is a no cost, globally resilient service.  You can ALLOW or DENY its identities on its AWS account.  It has no direct control on external accounts or users.  IAM lets you make use of identity federation and MFA.

An account root user is created by default when you create a new AWS account.  The account root user has full admin access to all settings and resources in an AWS account, thus, it is best to create a new IAMADMIN user that does not have full admin access to the account, just in case credentials are ever compromised.  You cannot restrict the permissions of the account root user.

The concept of restricting access privileges stems from the principle of least privilege. The principle of least privilege states that you should only give enough permissions for a resource to do its job and that's it!

Each AWS account features an instance of IAM, a globally available and resilient service that is free for all accounts.  The IAM of your account is fully trusted in your account.

IAM lets you create:

* **users** - represents humans or applications that need access to your account.  You pick IAM users when you pick individual things to log in to your account.
* **groups** - Collection of related users e.g. development team, finance, or HR
* **roles** - Can be used by AWS services, or for granting external access to your account.  If you want to grant services to interact with other services on your behalf, then use a role.

IAM policy document Allow or Deny's access to access service when you attach the policy to a user, group, or role.

IAM is an IDP and an authentication method.  IAM will authenticate the user and authorize them to operate on resources, which is based on policies attached to the user, group, or role.

## IAM access keys

* Long term credentials
* Used when accessing via CLI, API, etc.
* An IAM user can have two access keys
* Access keys can be created, deleted, made inactive, or active.  They are set active by default.

There are two parts to access keys, an Access Key ID, and a Secret Access Key.
