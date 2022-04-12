# S3 Basics

S3 is a global storage platform that is regionally based/resilient.  It can tolerate the failure of an AZ.
S3 is a public service, unlimited and multi-user.  Can handle movies, audio, text, large data sets
It's economical and accessed via UI/CLI/API/HTTP
It contains objects that are housed in buckets.

## S3 Objects

---

An object is a key-value pair, with the key being the name of the file, and the value is the content (zero to 5TB).

Objects have:

* A version ID
* Metadata
* Access Control
* Subresources

## S3 Buckets

---
The data inside an S3 bucket never leaves a region unless specified by a user.
S3 Bucket names are **globally** unique, and the bucket itself is infinitely scalable in a flat file format (all objects are at the same level -- there's no nesting)

## S3 patterns and anti-patterns

---

S3 is an object store, not file or block
You **can't mount** an S3 bucket.  S3 is great for large scale data storage, distribution or upload

## Highlights

---

3-63 characters, all lower case, no underscores.  Must start with lowercase letter or a number
There is a soft limit of 100 buckets per account, and a hard limit of 1000 buckets per account.

Unlimited objects in the bucket, from 0 bytes to 5TB

Key = name, value = data
