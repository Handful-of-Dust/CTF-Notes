# Web Shells

The idea is that you upload a bit of code that, when accessed, allows you to execute commands on the target machine. I haven't seen too many of these types of challenges in CTF competitions yet, but that doesn't mean I won't.

## How to upload a web shell

Sometimes it's as simple as finding the upload form on the site and using it to upload your file. Of course, in real life, websites should have some form of security to prevent you from doing exactly this.

## How to use a web shell once you have uploaded it

At the most basic level, you would go to the directory where the web shell has been uploaded (for example, <http://examplesitethatdoesntexist.com/uploads/shell.php>) and then append you command to the end of the URL as a query parameter, like this: <http://examplesitethatdoesntexist.com/uploads/shell.php?cmd=whoami>
