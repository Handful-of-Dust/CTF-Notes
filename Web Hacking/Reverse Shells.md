# What is a reverse shell and why would you use one?

A reverse shell connects back to your (the attacker's) machine when it is executed. Of course, you need to set up a listener before this happens. This is generally easier to sneak through a firewall because the initial connection is outbound, though this usually doesn't matter for simple CTF challenges.

## Setting up a listener

Netcat is probably the easiest tool to use for this. The syntax is simple: `nc -nvlp <port>`

You would simply replace the "port" placeholder with the port you instructed your reverse shell to connect back to: `nc -nvlp 4444`