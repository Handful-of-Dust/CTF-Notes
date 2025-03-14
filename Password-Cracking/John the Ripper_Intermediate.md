# Tips and Tricks for using John the Ripper

## Opening password-protected files

Often, CTF competitions will include password-protected files. John the Ripper can extract and crack password hashes from many different formats.

### PDF

`pdf2john protected.pdf > pdfhash.txt`

This extracts the hash and saves it in a new file, pdfhash.txt, which is formatted for John the Ripper. You can then run the following command to hopefully crack the hash: `john --wordlist=/usr/share/wordlists/rockyou.txt pdfhash.txt`

### Zip Archives

`zip2john protected.zip > ziphash.txt`

As in the previous example, you should then be able to crack the hash.

### RAR Archives

`rar2john protected.rar > rarhash.txt`

## /etc/shadow hashes

In Linux operating systems, the /etc/shadow file is where password hashes are stored. You need root privileges in order to access it.
