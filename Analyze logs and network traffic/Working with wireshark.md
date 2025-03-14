# If your file ends in .pcap or .pcapng...

That means you're going to be working with [Wireshark](https://www.wireshark.org/docs/). Because it's so common, I've compiled a list of my most commonly used Wireshark features.

## What to do first

Click the statistics menu and take a look at some of the basic qualities of the capture, making notes of what you find. Even if there aren't any questions that directly ask for this information, knowing, for example, the number of endpoints in the capture could come in handy. In particular, check the following:

* Statistics > Capture File Properties for the hash of the file and time of first and last packet
* Statistics > Conversations for an overview of who is talking to who. Even if you don't have a question on this, it can help you identify what parts of the file are likely most interesting
* Statistics > Endpoints to see how many devices there are
* Statistics > Resolved Addresses to see any websites visited or see which mac addresses correspond to particular hostnames. You can also see any comments on the pcap file here

## Other useful functions

If you know the number of a packet you want to look at but don't want to scroll to it, you can click Go > Go to packet and enter the number of the packet in the box that appears just under the display filter bar.

If you are hunting for a partular string in the contents of a packet, you can find that by clicking Edit > Find Packet. On the dropdown, you can choose whether you're searching via display filter, hex value, string, or regular expression. Then you can enter the data you want to search for. This is useful if you want to find all instances of clients sending a POST request to a server or something like that. 

If you've found an interesting packet, right click it and select Follow > TCP stream (or whatever the protocol happens to be). Always do this, even if you don't think it will be useful. 

## Using display filters

* You can use boolean operators (AND, OR, etc.) to join multiple queries
* Use != for negation
* You can use ip.src == to find all packets with a particular source IP, ip.dst == to do the same with destinatin IP, or just ip.addr == to find all packets that contain a particular IP address. 
* You can also filter for ports (for example, tcp.port eq 443)
* [More information here](https://wiki.wireshark.org/DisplayFilters)

## Extracting files from Wireshark captures

This is actually not an uncommon CTF question. To do this, find one of the packets in which the file data is shared and follow the protocol stream. Then, in the popup window, select "Raw" at the "Show data as" menu and select "Save as." You should then be able to open the file (if you don't know what kind of file it is, you can use the file command in Linux to identify it and then add the appropriate extenstion). You can also try File > Export Objects from the menu at the top.