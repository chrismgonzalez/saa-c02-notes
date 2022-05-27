# S3 Storage Classes

## S3 Standard

---

* Objects are replicated across 3 AZs in the AWS region.
* 99.999999999% durability (11 9's)
* Replication over 3 AZ's & Content-MD5 Checksums and Cyclic redundancy checks (CRCs) are used to detect and fix any data corruption issues
* S3 Standard as a 'milliseconds' first byte latency and objects can be made publicly available
* With S3 standard, you are billed a GB/month fee for data stored.  A $ per GB charge for transfer OUT (in is free) and a price per 1,000 requests.
* No specific retrieval fee, no minimum duration, and no minimum size
* API responds with a 200 OK when your data is stored successfully
* Use S3 Standard for Frequently Accessed data which is important and Non-replaceable

## S3 Standard-IA (infrequent access)

---

* Shares many of the same characteristics of S3 Standard except:
  * has a cost per GC data retrieval fee, overall cost increases with frequent data access
  * Minimum duration charge of 30 days - objects can be stored for less, but the min billing always applies
  * has a min capacity charge of 128KB per object
* Should be used for long-lived data, which is important but where access is infrequent

## S3 One Zone - IA

---

* Same as Standard IA, but data is only replicated to 1 AZ. Cost goes down, risk of data loss goes up.
* Should be used for long-lived data, which is NON-CRITICAL & REPLACCABLE but where access is infrequent.

## S3 Glacier - Instant

---

* Like S3 Standard-IA...cheaper storage, more expensive retrieval, longer minimum
* Min duration of 90 days
* Should be used for long-lived data, accessed once per quarter, with millisecond access.

## S3 Glacier - Flexible (cold storage)

---

* Objects cannot be made publically accessible, data access beyond object metadata requires a retrieval process
* Data in Glacier Flexible is retrieved to S3 Standard-IA temporarily (first byte latency = minutes or hours)
  * Expedited (1-5 min)
  * Standard (3-5 hours)
  * Bulk (5-12 hours)
  * Faster = more expensive
* Used for archival data where frequent or realtime access isn't needed (e.g. yearly) minutes to hours in retrieval time.

## S3 Glacier - Deep Archive (frozen storage)

---

* Objects cannot be made publically accessible, data access beyond object metadata requires a retrieval process
* Data in Glacier Flexible is retrieved to S3 Standard-IA temporarily (first byte latency = hours to days)
  * Standard (12 hours)
  * Bulk (48 hours)
  * Faster = more expensive
* Used for archival data that rarely if ever needs to be access - hours or days for retrieval, legal or regulatory data storage

## S3 Intelligent-Tiering

---

5 Storage tiers:

* Frequent Access
* Infrequent Access
* Archive Instant Access
* Archive Access (optional)
* Deep Archive (optional)

Intelligent tiering monitors objects to move their storage tiers based in frequency of use.

Intelligent tiering has a monitoring and automation cost per 1,000 objects.  Frequent access tier costs the same as S3 Standard, the infrequent the same as Standard-IA.  Archive Instant, Archive, and Deep Archive are comparable to their S3 glacier equivalents.

Designed to be used for long-lived data, with changing or unknown patterns.

### Documentation

[pricing](https://aws.amazon.com/s3/pricing/)

[Storage classes](https://aws.amazon.com/s3/storage-classes/)