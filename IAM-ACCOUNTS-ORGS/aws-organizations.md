# AWS Organizations

AWS Organizations are a great way to manage multiple AWS accounts, which is handy for large enterprises where there are many accounts.

When you create an organization from your AWS account, your account then becomes the **management account** (previously called the master account)

**Organization Root** (not to be confused with the root user) is a container within an AWS org that can contain accounts, it can also contain other containers, known as OUs (Organizational Units).

If you create an account from within the AWS organization, it is much easier than doing it from outside the org and inviting an account in (user must accept the invite)

Best practice - have single account to login to (in the management account, a single identity.  Large enterprise orgs use identity federation, like on-prem SSO).  For smaller organizations, users can log in to the login account and then role switch into other accounts.  The role switch essentially allows the user to assume a role in another account allowing the user to access the resources in that account.

Benefits of Organizations:

- Consolidated billing allows member accounts of an AWS organization to pass their payment data up to the payment account.  It allows a single monthly bill to be generated that holds all billing data for all accounts within an AWS organization.
- Certain services get cheaper the more you use them.  These benefits allow you to prepay for reservations and service usage.
