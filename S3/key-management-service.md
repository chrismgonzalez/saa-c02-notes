# Key Management Service (KMS)

* Regional & Public Service
* Create, Store, and Manage Cryptographic keys
* Symmetric and Asymmetric keys
* Cryptographic operations (encrypt, decrypt, etc...)
* Keys never leave KMS - Provides FIPS 140-2(L2)

## Customer Master Keys (CMK)

* Container for keys
* CMK is logical - ID, date, policy, desc & state
* Backed by physical key material
* Generated or imported
* CMKs can be used for up to 4KB of data

*CMKs are isolated to a region & never leave
**AWS** managed and **customer** managed CMKs
Customer managed keys are more configurable
CMKs support rotation
AWS managed keys rotate every 1095 days (3 years)
Customer managed keys rotate every year.

## Data Encryption Keys (DEKs)

* GenerateDataKey - works on > 4KB
* KMS does not store the DEKs
* Plaintext version
* Ciphertext version
* Then discard plaintext key
* Store encrypted key with data

## Key Policies and Security

Key policies (resource)
Every CMK has one.
Key Policies + IAM polices
Chain of trust: KMS has to be explicitly told that the key trusts the account that they're in. 
