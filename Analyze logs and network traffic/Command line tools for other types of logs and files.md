# What to do when you have a file that isn't a pcap

## Cat and grep are your friends

`cat` (short for concatenate) displays the contents of a file in your terminal. If it's a very long file and you're looking for something specific, this is actually not very useful. This is why you would pipe that command to grep in order to only display lines that contain the string you are interested in, like this: `cat reallylargefile.txt | grep interestingdata`

If you are interested in the number of occurences of a specific string, you can find the wordcount with the `-wc` flag like this: `cat reallylargefile.txt | grep -wc interestingdata`

## wc (Word Count)

`wc` can be used to find the number of words, lines, words, characters, and so forth. Those are the three values it displays by default.

## Sort

Sort does what it sounds like it does: it sorts the data in your file. It has lots of different flags that let you sort in different ways:

`-u` removes duplicates, providing only unique entries. For example: `cat largefile.txt | sort -u`

`-d` sorts in dictionary order and `-n` sorts numerically. `-r` sorts in reverse order.

Some extra resources: [Man pages for the command](https://www.man7.org/linux/man-pages/man1/sort.1.html) and [an explainer article with lots of examples](https://www.geeksforgeeks.org/sort-command-linuxunix-examples/)
