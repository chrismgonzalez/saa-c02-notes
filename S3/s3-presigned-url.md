# S3 Presigned URLs

Presigned URL's are a feature of S3 which allows the system to generate a URL with access permissions encoded into it, for a specific bucket and object, valid for a certain time period.

* Presigned URLs can be used for download (GET) or upload (PUT) requests.

Another use-case for Presigned URLs you can keep your bucket private.  The account can have an IAM user for an application.  When a request is made for an object, the IAM user requests the presigned URL from S3 and sends it back to the user.
