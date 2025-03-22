# Common Challenges

In CTF events, it's not uncommon for some of the challenges to involve files that are messed up in some way (maybe the magic bytes are messed up, or maybe there is a second file embedded in the data of the main file). Your task is usually to identify and fix the issues so that you can open the files and get the flag. Sometimes you might also be given a disk image and asked to look inside it for a particular file. Even simpler challenges might involve checking file metadata for information.

## Command Line Tools

### Exiftool

A very useful utility for examinging file metadata. Many challenges ask for details that are in the metadata of a file, such as timestamps or comments.

### File

A Linux command-line tool for checking the type of a particular file. This can be useful if you have a file that doesn't have an extension or has an incorrect one. Example: `file fileofinterest.extension`

### Binwalk

A tool for finding data embedded in files. The basic syntax is `binwalk nameoffile.extension -flag`. The [man page](https://www.kali.org/tools/binwalk/) shows all of the many flags that are available. The ones I use most frequently are `-e` (to automatically extract any files binwalk can detect) and `-M`, which recursively scans extracted files.

### xxd

Tool for creating hex dumps from files. This can be useful if you are given a file that won't open. It could be that the data inside (usually some of the bytes that form the file signatures) has been corrupted, and you may have to repair it manually. For example: `xxd messedupfile.png` will create a hex dump of messedupfile.png. It also has some [options](https://www.geeksforgeeks.org/xxd-command-in-linux/). To save the hexdump as a new file, you would want to do this: `xxd badfile.png > hexdump.hex`. You could then open the hexdump in the text editor of your choice and edit both the bytes and the ASCII representation to fix the underlying problem. Then you would use `xxd -r hexdump.hex fixed.png` to convert the hexdump back into a binary file, which you should be able to open.

## Tools with a graphical user interface

### Autopsy

Tool for opening disk images.

## Online Tools

Note that you can use these on a host machine or personal VM as long as it is connected to the internet, but many CTF challenges will include VMs that do not have internet access, limiting you to tools that are included on the VM (usually simple command line tools like the ones described above).

### List of File Signatures

I come back to this [Wikipedia page](https://en.wikipedia.org/wiki/List_of_file_signatures) at least once every challenge.

### Online Hex Editor

I like [Hexedit](https://hexed.it). It's easy to use and handy when you don't have a hex editor installed on your host machine.

### CyberChef

CyberChef is a bit of an exception because it does have an offline version that you can install, but that might not be usable in challenge VMs. You can access it [here](https://gchq.github.io/CyberChef/). It is most heavily used for cryptography challenges, but it does have some tools that can be used to work with files. Under Forensics on the "Operations" pane, the recipes I use most often are "Scan for Embedded Files" and "Extract Files."
