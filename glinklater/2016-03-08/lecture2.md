# Lecture 2 - Cryptography

## History of Cryptography

* Cryptography
  * Science of secret writing
  * Greek: Kryptos Graphia
  * Hiding what you are writing
* Cryptoanalysis
  * Science of breaking ciphers
* Cryptology
  * Encompasses both subjects

## Ancient History

* Egypt 1900BC non-standard hieroglyphs
* Mesopotamian tablet 1500BC
* Hebrew scripts -> substitution cipher ATBASH (500-600BC)
* Greece 487BC -> skytale
* Caesar Cipher (50-60BC) -> substitution cipher with normal alphabet, shift n places to encode, shift a few more to decode
* 725-790AD Arabic mathematician wrote a book on Cryptography.
* Roger Bacon (1250AD) "A man is crazy who writes a secret in any other way than one which will conceal it from the vulgar"
* 1466-1467AD designing a cipher disk.
* 1518AD Johannes Trithemius wrote the first printed book on Cryptology. Invented a steganographic cipher in which each letter was represented as a word taken from a succession of columns.
* 1553AD Glovan Batista Belaso -> Vigenere cipher
* 1563AD Glovanni Battista Porta wrote a text on ciphers, introducing the diagraphic cipher.
* 1790AD Thomas Jefferson invented wheel cipher. Used in WW2
* 1854AD Charles Babbage reinvented wheel cipher.
* 1913AD Captain Parket Hitt reinvented wheel cipher.
* 1917AD Gilbert S. Vernam, invented practical polyalphabetic cipher machine capble of using a key which is totally random and never repeats.
* 1918AD The ADFGVX system was put into service by the germans in WW1.
* 1923AD Arthur Scherbius -> Enigma Machines
* 1927-1933AD American Prohibition -> "The greatest era of international smuggling -- prohibition -- created the greatest era of criminal cryptography"
* 1976 Introduce asynchronous encryption.
* 1977 Diffie-Hellman Key Exchange -> RSA created
* 1984-1985 ROT13 -> USENET News server software.
* 1991 Phil Zimmermann -> PGP (Pretty-good-privacy)
* 1994 The blowfish cipher is described by Bruce Schneier
* 1997 NIST looks to replace DES.
* 1998 AES standard evaluation.
* 1999 Rijndael chosen to be AES standard.

## Perception of Encryption

* With the advent of ecommerce and the use of crypto in every day life the perceptions and needs have changed.
* Traditionally, encryption as used to prevent a third part gaining access to information in transit.

## Definitions

* Plaintext
* Cipher text
* Crypto system -> a system that provides encryption and decryption
* Algorithm
* Key -> the random comppnent used to seed the encryption algo.
* Key space -> potential pool of possible keys
* Key clustering -> when >1 keys produce the same cipher text
* Work Factor -> how hard an algorithm is to break in terms of resources.

## Keys - Questions to ask

* Choosing the right key is essential to any form of encryption?
* Where are the keys generated?
* How are the keys generate?
* Where are the keys stored?
* How do they get there?
* Where are they keys used?
* How do we replace a lost key?

### Keyspace

It is a bad idea to have a small keyspace... more entropy === better

## Classical Cipher Systems

* Substitution Ciphers
* One-time pad (Vernam Ciphers)
* Uses modulo addition
* Book / Running Key
  * Large body of text
  * Vulnerable to redundancy
* Codes
  * Construction of words/phrase mappings to other phrases, number of symbols.
* Stengography
  * From the greek for covered writing
  * Hiding the existence of a message
  * Microdots, watermarks.
* Encoding is not the same as enciphering.
* Encoding is when there is a symbol exchange. Usually involves a code book of some kind.

## Symmetric Encryption

* Plaintext is encrypted using a secret key
* Ciphertext is decrypted using the same key.

* The process makes use of public and private compontents.
* Public
  * Algorithm to be used
  * The cipher text
* Private
  * The key to be used
  * The exact transformation used out of a number of possibilities.

## Asymmetric Encryption

* Makes use of multiple keys for greater security, and solving the problem of key distribution
* Each part has their own keypair, obviating the need for a shared secret key
* Bases on the work by Diffie & Hellman Rivest, Shamir & Adleman
* Finding large prime factors of numbers is a problem.
* Some points to note
  * Public key cannot decrypt a message it encrypted
  * Ideally a private key cannot be derrived from a public key.

## Strengths and Weakness

### Asymmetric

* Strengths
  * Better key distribution
  * Scalability
  * Provides confidentially, authentication, non-repudiation
* Weaknesses
  * Slower and more resource intensive than symmetric systems.

### Symmetric

* Strengths
  * Faster than asymmetric systems
  * Hard to break if sufficiently large systems
* Weaknesses
  * Key distribution
  * Scalability
  * Limited security
    * Confidentially only
    * No Authentication or non-repudiation

## Goals of crypto

* Confidentially
* Authentication
* Integrity
* non-repudiation
  * Sender and Recipients cannot deny having sent or received a message

## Maths

As long as we know XOR we're fine.

## Properties of a Cipher

* Confusion
  * Strong keys cause confusion by introducing unknown values
* Diffusion
  * Plaintext input is put through mant functions and components are therefore dispersed.
* Reduced redundancy
* Fair statistical distribution

## Are all ciphers the same?

* Different applications have needs for different ciphers, or ciphers operating in different mods.
* Block
  * Used for encrypting blocks of data such as files
* Stream
  * Operate one bit or character at a time, length of data unknown.

### Block Ciphers

* Can be used for encryption and decryption purposes
* Messages are divided into blocks of bits.
* Each block is encrypted in parallel
* Makes use of confusion and diffusion
* Substitution-Boxes are often used
* Better suited to software implementations
* Some can operate in a stream cipher emulation mode.

### Stream Ciphers

* Cipher operates on much smaller comonents of a message, usually bit or byte level.
* Uses a key stream and XOR with each bit as it comes in.

## Hashing

* Reduction functions used to tranform a message of arbitrary length to a fixed length 'fingerprint'
* Based around a one-way function
  * y=F(x) is easy
  * x=F\`(y) is not
* A crypto hash is a digital fingerprint for a message
* Reduces a large volume of input data down to a 'unique' array of bits.


* Ease of computation
* Compression -> fixed output
* Pre-image resistance
  * One way
  * Weak collision resistance
* Two flavours
  * One-Way OWHF

### Goals

* Provides Integrity.
