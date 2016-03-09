# Lecture 3

## Public Key Crypto

* Asymmetric Enc. is slow but is useful to encrypt symmetric keys.
* Symmetric key is fast but has the problem of distributing keys.


## Sending a Message (PGP)

1. Alice writes a message
* Alice generates a symmetric key
* Alice encrypts message using symmetric key
* Alice hashes the cipher text and signs it using her private key
* Alice encrypts the symmetric key with the Bob's public key and sends him the entire message with signature, payload and encrypted symmetric key.
* If Alice wants to send the same message to other people then she can simply encrypt the symmetric keys with their public keys and send the whole thing to them as well.

## Public Key Infrastructure

* NOT PKC (not public key cryptography)
  * SMPT vs Email Infrastructure
  * SMTP does not provide all the different protocols and storage.
* Provides:
  * Authentication
  * Confidentially
  * Integrity
  * non-repudiation
* Hybrid Crypto Systems

## Certificate Authorities

* CA is an organisation that maintains and issues public key certificates.
* CA is trusted by people to perform some kind of verification on clients.
* I trust you because the CA trusts you
* Should maintain a Certificate Revocation List (CRL)
* Work with registration authorities (RA)
* Multiple certificates for improved security.

## PKI Gives us

* Confidentially
* Access Control
* Integrity
* Authentication
* Non-Repudiation

## Digital Signatures

* Encrypt a hashed message with private key
  * RSA
  * DSA
* Hashing
* SHA2 & SHA3

## Attacks on Hashing

* A hash function produces the same message digest for two different messages in a collision
* Observed collisions lessen the security of the cryptographic method.
* Similarly, it's very hard to create a message for a given digest.
* However, it's orders of magnitude easier to create two messages that share a hash.

## Key Storage

* Keys are stored pre and post-distribution
* Where is a secure place to store a key?
* Traditionally you moved them in a locked box
* Now most distribution is via automated process over secure channels.

## Good key practice

* Like passowrds, cryptographic keys require some care and feeding
* Keys should be periodically changed
  * Often forced through expiry
* Keys shoudld be verified, and expired
  * Security dictates the frequency
* The change and communication of that change be secure.

### Management Principles

* Key length should be long enough to provide the necessary protection required
* Transmissions and storage sould be secure.
* Keys should be random, and utilise the full reach of the key-space
* Lifetime of a key should be related to the sensitivity of the data being protected
* The more frequent the use, the shorter the lifetime. Why?
* Keys should be backed up or Escrowed
  * Split key into M parts
  * Set N s.t. M>=N
  * Any N parts can recover the key.
  * #Meth
* Keys should be properly destroyed at end-of-life

## Link vs. End-to-End

* Encryption can be implement a two levels
* Link
  * All data on comms path is encrypted.
  * Include all packet headers, payloads, trailers, etc.
  * Proivdes CIA to all
  * IPSEC


* End-to-End
  * Application layer, only payloads encrypted.
  * Headers and other addressing information still visible.
  * S/MIME

### Link Layer

* Advantages
  * All data encrypted, users don't have to do anything


* Disadvantages
  * Data is decrypted and reencrypted at each node.

### End-to-End

* Advantages
  * Protection from Start to Finish
  * User discretion / flexibility as to what gets encrypted, and how
  * Higher granularity due to increased keys
  * Messages not decrypted at each hop


* Disadvantages
  * Headers, addressing, routing info not protected -> leakage
  * Destination systems need appropriate config end-users.

## Cracking Crypto

* Passive Attacks
  * Attacker is not affecting keys, protocol, algorithm used, or the messages being passed
  * Very hard to detect, and relatively easy to mount, impossible to detect.
    * Often a pre-cursor other things
  * Prevention rather than detection
  * Examples
    * Sniffing
    * Eavesdropping
    * Data capture and interception


* Active Attacks
  * Modification of file, data streams and masquerading as another party, attacker is actively involved.
  * Cipher text-only
  * Known-plaintext
  * Chosen-plaintext
  * Chosen-Cipher text
  * Main in the middle
  * Dictionary
  * Replay
