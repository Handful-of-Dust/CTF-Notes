# Hashcat Basics

Hashcat can be quite fast if you use your GPU (doing this on your host machine is recommended). It can be run on Windows as well as Linux.

## Hash types

You need to use the -m flag to tell hashcat what type of hash you're trying to crack. You use a number to indicate the type of hash. Here's a [list of numbers](https://hashcat.net/wiki/doku.php?id=example_hashes).

## Hashcat on Linux

`hashcat -m hash_type -a attack_mode hash.txt wordlist`

## Hashcat on Windows

This is a bit more complicated. You will need to [download hashcat](https://hashcat.net/hashcat/). Once you have extracted the file, you can right-click "Open in terminal" and run hashcat as follows: `.\hashcat.exe -m hash_type -a attack_mode hash.txt wordlist`

You may want to make a folder inside the main hashcat folder to contain your hash.txt files and another folder to contain your wordlist(s). I found [this tutorial](https://www.linkedin.com/pulse/introduction-password-cracking-hashcat-jonathan-mooney-p8ste/) helpful.

Note: I initially saved the hashcat folder to my desktop and was able to run it successfully once before getting a "permission denied" error. Hashcat doesn't seem to be able to run from any location that syncs to OneDrive.
