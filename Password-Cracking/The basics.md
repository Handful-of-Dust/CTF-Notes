# How it works

Basically, hashing algorithms are one-way math. They are designed to represent a user's password and thus verify the user's identity without revealing the user's password.

## Identifying Hashes

If you are using Kali Linux, hashid should be preinstalled. You can use it to determine what kind of hash you're dealing with. If you only have a hash and no other identifying information or formatting, you will need to specify what kind of hash it is in order to use John the Ripper, so this step is important. Fortunately it's quite simple: `hashid f2528d1e9a5bf0528c4e4a5a58becd8c93114adc`

## Easy ways to attack

### Rainbow Table

For old hashing algorithms, or simple ones, it is reasonable to check an online rainbow table to see if they can be cracked.
[hashes.com](https://hashes.com/en/decrypt/hash)

### John the Ripper

Frequently used with the rockyou.txt wordlist, located at /usr/share/wordlists/ in Kali Linux and some other distros as well.
    `john --wordlist=/path/to/wordlist hash.txt`

### Hashcat

Basic syntax:
    `hashcat -m hash_type -a attack_mode hash.txt wordlist`

[Good basic tutorial](https://www.freecodecamp.org/news/hacking-with-hashcat-a-practical-guide/)
