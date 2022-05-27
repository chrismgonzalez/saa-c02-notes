# S3 Presigned URLs

Presigned URL's are a feature of S3 which allows the system to generate a URL with access permissions encoded into it, for a specific bucket and object, valid for a certain time period.

* Presigned URLs can be used for download (GET) or upload (PUT) requests.

Another use-case for Presigned URLs you can keep your bucket private.  The account can have an IAM user for an application.  When a request is made for an object, the IAM user requests the presigned URL from S3 and sends it back to the user.

## Exam tips for S3 Presigned URLs

* You can create a URL for an object you have no access to
* When using the URL, the permissions match the *identity which generated it*
* Access denied could mean the generating ID never had access..or doesn't now
* Don't generate with a role.. the URL will stop working when temporary crednetials expire.
