# Lecture 4

## Identification

* Subjects claimed identity must be verified
* Two phases in identification
  * Public - claimed identity
  * Private - verification
* Can be based on three primary factors
  1. Something you know (Password)
  2. Something you have (Token)
  3. Something you are (Biometrics)

## Better Passwords

* Cognitive Passwords
  * Fact or opinion based challenge response
  * Commonly used as a backup in the even of password loss. What is your dog's name?
* One-Time Password
  * A password that is generated systematically and only usable for a single instance
  ```
  94: BEAT WHEE CORD RISK JOBS ...
  95: ...
  96: ...
  ```

## Salty Passwords

* What is Salt?
* Why does salt improve things?
* Salt adds additional entropy to passwords.

## What is a good password?

* Length beats complexity

### Pass phrase

* Different from passwords
* Pass phrase is usually much longer and more complex
* More likely to remember because it makes sense
* Application takes a pass phrase and generates a 'virtual password' to be used in identity authentication.
  * e.g. ```IlikeMyGreenEggsWithoutHam```

## Tokens

* These are a physical piece of hardware
* Build on the One-Time Password
* Challenge Response-Based
* Require PIN entered and they ? time Synched OTP
* Other types store a digital certificate, and must be physically connected to a device (see U2F)

## Biometrics

* Verification of an individual (human) identity based on a unique physiological aspect of their person.
