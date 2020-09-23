+++
slug = "00_a_communications_protocol"
title = "A Communications Protocol"
date = "2020-04-06T10:44:01-04:00"
author = "Noah Kernis"
tags = ["itp", "critical_communications"]
description = "FILL"
showFullContent = false
+++

<!-- {{< figure src="img/..." alt="..." caption="[ ... ]" >}} -->

## Assignment

Research a communications protocol of your choice and write it up what you find in a blog post. Questions to answer (at the very least):

- How does it work?
	- Doesn't need to be super technical but it should be detailed enough that to understand how someone could use it.
- Who made it?
- Why was it made?
- What did you find interesting about it?

For the purpose of this assignment a communications protocol will be defined as a system of rules that allow two or more entities of a communications system to transmit information via any kind of variation of a physical quantity (Source: Wikipedia).

## Think

I decided for this assignment that I was going to research a communications protocol that was related to the internet. Originally I was keeping it broad, including things like Secure Shell (SSH) and File Transfer Protocol (FTP). 

*Initial Ideas:*

 - ARPANET
	- https://en.wikipedia.org/wiki/ARPANET
 - OSI
	- https://en.wikipedia.org/wiki/OSI_model
	- https://en.wikipedia.org/wiki/Internet_protocol_suite
- SMTP
	- https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol
- SSH
	- https://en.wikipedia.org/wiki/Secure_Shell
- FTP
	- https://en.wikipedia.org/wiki/File_Transfer_Protocol
	- https://tools.ietf.org/html/rfc354


After some initial research I decided that I wanted to focus on protocols that really make up the backbone of the modern internet as we have come to know it. The three that I narrowed down to were:

- [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)
- [DNS](https://en.wikipedia.org/wiki/Domain_Name_System)
- [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

*Transmission Control Protocol (TCP)*

I was interested in TCP for several reasons. One is that it was one of the initial protocols of the internet. Second, it establishes the connections that a lot of the modern internet runs on top of. It is an important protocol that lives in the background. 

*Domain Name System (DNS)*

DNS jumped out to me because it is a place where humans and computer can sort of communicate. The idea being, create human readable names that map to IP addresses for routing. It is an organizational protocol that also acts as a bridge between people and the infrastructure of the internet. 

*Hypertext Transfer Protocol (HTTP)*

HTTP was kind of an obvious choice. That said, it is how much of content and actual "meat" of the internet is transmitted. It sits on top of many protocols, but is fundamental to the actual information we send over the internet. 

After lots of pacing and ruminating I decided to go with TCP. Through my work experience I have had more exposure to the inner workings of HTTP. TCP will give me a chance to play around with the implementation of the protocol and to really engage with the history of the modern internet. 

## The Protocol: Transmission Control Protocol - TCP 

*Resources*

- [Out-of-Band Control Signals in a Host-to-Host Protocol](http://www.networksorcery.com/enp/rfc/rfc721.txt)
- [Original RFC: SPECIFICATION OF INTERNET TRANSMISSION CONTROL PROGRAM - December 1974 Version](https://tools.ietf.org/html/rfc675)
	- [761](https://tools.ietf.org/html/rfc761)
	- [793](https://tools.ietf.org/html/rfc793)
- [Network Sorcery](http://www.networksorcery.com/enp/protocol/tcp.htm)
- [W3C](https://www.w3.org/TR/tcp-udp-sockets/)
- [Julia Evans](https://jvns.ca/blog/2015/11/21/why-you-should-understand-a-little-about-tcp/)
- [OSI: The Internet That Wasn’t](https://spectrum.ieee.org/tech-history/cyberspace/osi-the-internet-that-wasnt)

*Who made it?*

The Network Working Group working on the original ARPANET. Many people were involved with various aspects and are reference in the original RFC. 

The RFC was written by Vinton Cerf, Yogen Dalal, and Carl Sunshine.

*Why was it made?*

> In a seminal moment in the development of the Internet, DARPA’s Robert Kahn (who joined the Information Processing Techniques Office as a program manager in 1972) asked Vinton Cerf of Stanford University to collaborate on a project to develop new communications protocols for sending packets of data across the ARPANET. That query resulted in the creation of the Transmission Control Protocol (TCP) and the Internet Protocol (IP), most often seen together as TCP/IP. These protocols remain a mainstay of the Internet’s underlying technical foundation. [DARPA](https://www.darpa.mil/about-us/timeline/tcp-ip)

*How does it work?*

Here is a high-level description of the protocol:

> The Transmission Control Protocol provides a communication service at an intermediate level between an application program and the Internet Protocol. It provides host-to-host connectivity at the transport layer of the Internet model. An application does not need to know the particular mechanisms for sending data via a link to another host, such as the required IP fragmentation to accommodate the maximum transmission unit of the transmission medium. At the transport layer, TCP handles all handshaking and transmission details and presents an abstraction of the network connection to the application typically through a network socket interface. [Wikipedia](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)

Here is a simplified example of how the protocol works:

> For example, when an email is sent over TCP, a connection is established and a 3-way handshake is made. First, the source send an SYN “initial request” packet to the target server in order to start the dialogue. Then the target server then sends a SYN-ACK packet to agree to the process. Lastly, the source sends an ACK packet to the target to confirm the process, after which the message contents can be sent. The email message is ultimately broken down into packets before each packet is sent out into the Internet, where it traverses a series of gateways before arriving at the target device where the group of packets are reassembled by TCP into the original contents of the email. [CloudFlare](https://www.cloudflare.com/learning/ddos/glossary/tcp-ip/)

...

*What did you find interesting about it?*

The most important thing about TCP to me is how fundamental it is to the modern internet. It is a protocol used by so many people so often - and it may as well be invisible. 

Some of the language involved in describing the protocol (for example, the three-way handshake) embeds a western cultural greeting into the exchange of data.

TCP (and IP) were mentioned all the time when I worked as a DevOps engineer. The truth is I know they exist and the basics of how they work, but I don't actually have a concrete understanding of the mechanics.

These are some of my initial thoughts about what I want to explore:

- I'm interested in first, understanding how it works. I want to actually implement the protocol myself.
- Second, I want to know the limitations of the protocol. What constraints does it have? How does that effect the information sent over it? Or what can even be sent over it?
- Third, I want to understand the world and life-cycle of the protocol. Not only how it works, but what pieces of infrastructure must it pass through? How long does it "live"? How does it change when sent, received, etc?
- Fourth, how can I tamper with it? How resilient is it to tampering? What happens to data when the protocol can't complete? Where do "lost" packets go?
