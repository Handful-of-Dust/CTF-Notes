# This is what you should do first

Before you get carried away, take a look around to understand what you're working with. I'm taking some inspiration here from my notes on a TryHackMe room, but also adding my own content.

## 1. View Page source

Take a look at the HTML and determine whether there's anything interesting. Comments, scripts and so forth can give you clues. If the name of the challenge doesn't give you a hint about what angle you're supposed to be taking, this might.

## 2. Use the Developer Tools

Personally, I really like Chrome's developer tools and use them for most challenges. Things to check in developer tools include:

* On the network tab, requests to and from the server (which can be helpful if you are trying to get around a login form or upload a specific type of file).
* The console, where you can interact with JavaScript in the webpage. If the challenge uses some form of client-side authentication, for example, you may be able to print valid credentials with the console using `console.log(variable)`.
