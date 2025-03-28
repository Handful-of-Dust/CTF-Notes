# Encoding data

When data is encoded, it's really just put in a different format so that it can be processed in some way by a computer. Encoding is easily reversible and not at all the same thing as encryption, where the goal is to prevent data from being read by anyone who isn't authorized to access it, but it still shows up in easy cryptography challenges sometimes. Again, CyberChef is probably the easiest way to tackle most of these challenges, but there are command line tools that you can use (and should probably know how to use just in case) as well.

## Recognizing Types of Encoded Data

### Binary

Will usually be pretty easy to identify since it's just ones and zeroes.

### Decimal

If you see a series of numbers that don't look like a substitution cipher and they're all between roughly 97 through 122 (numbers outside of this range are likely special characters), you may be looking at decimal numbers that represent ASCII characters. This is pretty easy to solve; CyberChef has a "from decimal" recipe.

### Base64

Base64 is quite common and easy to recognize. It contains the following characters: A-Z, a-z, 0-9, +, /, =.
