# S3 Encryption

Encryption is not defined at the bucket level, it is defined at the object level.

## Client-Side Encryption (encryption at rest)

* Objects are encrypted on the client side before it is in transit to S3.
* The user has control over the encryption lifecycle.

## Server-side encryption (encryption at rest)

* Objects do not arrive to S3 encrypted.
* Handles some or all of the encryption process.

There are 3 types of SSE in S3.

* **SSE-C - Server-side encryption with Customer-Provided Keys**
  * S3 handles the encryption process
  * Customer provides the object and the encryption key
* **SSE-S3 - Server-side encryption with Amazon S3-Managed Keys**
  * S3 handles the whole encryption process
  * A unique master key for every object uploaded, each new object receives a different master key
  * The user has very little control over the encryption details
  * Less admin overhead
  * The user does not control key rotation, which is managed by S3
  * Uses AES256 encryption algorithm by default
* **SSE-KMS - Server-side encryption with Customer Master Keys (CMKs) stored in AWS Key Management Service**
  * S3 still manages encryption lifecycle
  * Keys stored in KMS
  * A single CMK is used to encrypt all objects
  * The user can have fine grained control over key settings and rotation
  * The user can role separation. Allows for there to be S3 admins that cannot have access to decrypt objects within S3 buckets

### Documentation

---

[Default Bucket Encryption](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/default-bucket-encryption.html)

[S3 services](https://docs.aws.amazon.com/kms/latest/developerguide/services-s3.html)

[Using KMS Encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html)

[Using Server Side Encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingServerSideEncryption.html)

[Server side encryption with CMKs](https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerSideEncryptionCustomerKeys.html)
  