# The Basics of Asymmetric Encryption

With asymmetric encryption, the concept is that everyone involved in an exchange has a public key and a private key. In order to send a message to someone, you would first encrypt the message using the recipient's public key. That way, at least in theory, only the recipient could decrypt the message using his private key. A weakness with symmetric encryption is that the key needs to be exchanged between the parties involved, and it could theoretically be intercepted during this process. Asymmetric encryption gets around this issue.

## Breaking RSA

This is a pretty common challenge for CTF competitions. RSA relies on the factorization of prime numbers, but if the numbers are small enough, it can be broken.

In order to break it, you need to understand how the underlying math works. (technically, you can probably get by just by using tools, but it's best if you know what you're doing)

* n = p * q (p and q must both be prime numbers). n is the modulus of the public-private key pair.
* *ф*(n) = n - p - q + 1
* e is relatively prime to *ф*(n)
* e * d = 1 mod *ф*(n)

### Tools for breaking RSA

* <https://github.com/RsaCtfTool/RsaCtfTool>
* <https://github.com/ius/rsatool>

## PGP (Pretty Good Privacy)

PGP can be used to encrypt files or emails. Some CTF challenges involving PGP might only ask for you to look up a public key using a PGP public key database. Here's a good [walkthrough](https://trove.cyberskyline.com/8eb49cf698d149fe969acd161020245d) that also links to some lookup databases.

You might also be asked to decrypt something that has been encrypted with PGP. You can do this with GPG, but you'll need the key.
