# S3 Static Hosting

Accessing S3 is generally done via APIs

Static Website Hosting is a feature of the product which lets you define a HTTP endpoint, set index and error documents and use S3 like a website.

In order to take advantage of S3 static hosting using a custom domain, the custom domain must be in Route53 and the bucket name must match the domain name.

Keep in mind that operations on an S3 bucket do incur a cost.
