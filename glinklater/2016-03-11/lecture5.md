# Guest Lecture (DFIR)

## Digital Forensics

* Incident ->
* Detected ->
* Identification (usually skipped by corporates) ->
* Remediation ->
* Report ->
* Incident -> and so on...

## Identification

* Corporates usually skip identification due to the fact that they're paranoid.
* Remediation is usually a loud process that tips the fact that the breach has been detected and gives attackers a chance to change their modus operandi (MO).

## Incident Response

* Used to demonstrate due dillegence to gov. agencies.

## Digital Forensic Process

* Acquisition ->
* Examination ->
* Analysis ->
* Report

## Memory is Important

* Memory contains things like keys for full-disk encryption.

## Places to get data from

* User directory (all files that are created by the user)
* Registry (ties to user data)
* Windows Directory (sys32/config)
* See diagram

## Analysis

* Reconstruct system activity over a period of time.

# Lecture 5

## Biometric Ranking

### Effitiveness

1. Palm scan
* Hand Geometry
* Iris scan
* Retina scan
* Fingerprint
* Voice print
* Facial scan
* Signature dynamics
* Keyboard dynamics

### Acceptance

1. Iris scan
* Keyboard dynamics
* Signature dynamics
* Voice print
* Facial scan
* Fingerprint
* Palm scan
* Hand Geometry
* Retina scan

## Biometric Errors

* Type 1
  * False rejection rate
* Type 2
  * False acceptance rate
* Crossover Error Rate (CER)
  * Where FRR === FAR

## Cryptographic Keys

* Strong public key enc. is used to generate key pairs
* Identity Authentication is based on them being a matching crypto key-pair.
* Commonly used protocols like SSH

## Memory and smart cards

* Differ only in processing power on-board smartcard has a functional CPU
* Both have Memory
* Simplest form is an ATM card
* Smartcard can be used to provide secure authentication using a challenge-response
  * Home affairs use biometric and cryptographic keys on your ID card

## Authorisation

* Different from authentication
* Authentication -> Verifying idenity
* Authorisation -> Validating that the subject is allowed to perform a specific action.

## Access Criteria

* Access criteria should be as fine grained as possible
* Fine grained === huge complexity
* Access criteria are the rules used in the authorisation process
* Prevent 'access creep'
  * Revoking privilege is a real problem.
* Roles
  * Tied to a role that filled rather than a person
* Groups
  * Certain groups of people get permissions
* Physical/Logical location
  * It depends where you are
  * Geolocation is fairly accurate (at least to the country level)
* Time of Day (Environment)
  * Access only granted during specific hours
* Transaction Type
  * Certain classes of transaction may be granted and other forbidden

Principal of least access -> black and whitelisting

## Reliable Defaults

* Know your default
  * Default allowed
  * Default deny
* Deny is safer as it catches anything not explicitly allowed
* Protocols against unforseen holes
* Know how your system process Access Control Rules
  * List based
  * Chain based

## Least privilege

* Need to Know
  * If you don't need to know information in order to perform a task; information is withheld

## Single Sign-On

Single Sign-on provides a single point of initial authentication, and this is then propagated.

* Scripts
* Kerberos
* SESAME
  * Secure European System for Applcations in a Multi-vendor Environment
* Thin clients
* Windows Domains

## Access Control Models

* An ACM is a framework that dictates how a subject accesses objects

* Discretionary
  * User owns information they create
  * Ownership can be assigned
* Mandatory (MAC)
  * gives data owners some say in access to the data by others
  * The operating system has the final say in access control decisions
* Non-Discretionary
  * Also know as Role-based access control
  * Role-based or Task-based
  * Latice-Based
    * Determined by sensitivity level assigned to a Role
    * provision of an upper and lower sensitivity boundary

## Access control admin

* All this access control comes with a cost (admin)
* Centralised
  * RADIUS
  * TACACS/TACACS+
* De-centralised/Distributed
  * Security Domains
* Hybrid
  * Federations (TRUST REQUIRED!!!)
  * Miracle that eduroam works
    * No real legal enforcement between parties

## Security Domains

* A security domain is not a windows domain
* Subjects within share a common security policy, procedures and rules.
* Note this is slightly different to the Microsoft concept of a Network Domain
* Actual implementation of the doimain hierarchical.

## Access Control Layers

* Physical
* Technical

### Physical

* Network segregation
  * Physical split in network
* Perimeter security
  * Guard your borders
* Computer controls
  * Cable locks, drive locks -- even a lack of drives
* Work area separation
  * Restricted access separation of duties, need to know & least privilege.
* Data backups
  * Backup MUST happen -> secure, offsite and offline storage
    * RAID IS NOT A BACKUP SOLUTION
* Cabling
  * Prevention from damage, interception, theft
* Locks
  * ?

### Technical

* System Access
* Network Architecture
* Network Access

### Administrative

* Policies and Procedures
* Personnel controls
  * Separation of duties etc.

### Access Control Types

* Layered Defence
  1. Perimeter Security
  * Intrusion Detection
  * Username and Password
  * Access control lists
* Access controls can be classified as follows
  * Preventative
  * Detective
  * Corrective
  * Deterrent
    * Security cameras (if you know you're being watched then you're unlikely to do something wrong)
  * Recovery
    * Incident managment
  * Compensating
    * How do we fix things after incident?

### Good practice

Keep the least number of doors and windows open and you'll keep the flies out.

* Minimum accounts
* etc.

### Summary

* Access controls are your first line of defence. YOU NEED THIS.
* Critical to maintaining of system integrity and the CIA of the information contained within
* Controls can be of varying types
* One size does not fit all, org needs to find what works for them vs cost.
