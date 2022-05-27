# Encryption 101

## Encryption Approaches

* Encryption at rest
  * Designed to protect information in storage or physical devices like laptops/servers
* Encryption in transit
  * Aimed at protecting data in transit between locations

## Concepts

* **Plaintext** - unencrypted data
* **Algorithm** - A piece of math that generates encrypted data
* **Key** - An algorithm takes data + a key and generates ciphertext
* **Ciphertext** - What is generated when you take plaintext, an encryption algorithm and a key.  It is the stream of scrambled data

## Symmetric

* Symmetric keys are used as part of the symmetric encryption process. In symmetric encryption, both parties use the same key to decrypt the data.  This is vulnerable because if the key is leaked, the encryption is no longer protected.
* Symmetric encryption is great for local encryption on the same device, but not for encryption used for transit data.

## Asymmetric

* Asymmetric encryption uses different encryption keys (public key and private key)
* Public key is used to generate the encryption, which is then decrypted using the private key.
* Private key and the ciphertext are used together by the encryption algorithm to decode the data into plaintext

## Signing

* The process by which we can verify that the encrypted data was not tampered with, verifying that the data was signed using the private key of the location where the data came from.
* Signing is used to verify identity.

## Steganography

* Allows you to embed data in another piece of data in order to encrypt and decrypt data.
