# Networking models

Models are used to represent how networks function
There are 2 very popular network models:

1. OSI seven-layer model
1. TCP/IP model
_____

## OSI vs TCP/IP

#### OSI - There are 7 distinct functions a network must do

| Layer        |  Description                                                           |
| ------------ | ---------------------------------------------------------------------- |
| Physical     | what type of cables do i use?                                          |
| Data link    | everything that works with a MAC address: network cards, switches      |
| Network      | IP addresses: routers                                                  |
| Transport    | disassembles packets and makes sure they come through in a good order  |
| Session      | actual connection between 2 systems                                    |
| Presentation |  presents the data in a readable and presentable way                   |
| Application  | "logic and smarts": e.g Microsoft Office is network-aware              |

#### TCP/IP

+ Network interface - all physical cabling, MAC addresses, network cards, other hardware & routers
+ Internet - IP address
+ Transport - assembly and disassembly and anything it takes to connect to the system and make sure the files have arrived safely
+ Application - old OSI application, presentation and session layers
_____

## Walking through OSI and TCP/IP

#### Client to server example

| Flow                                                                                           | TCP/IP stage | OSI stage |
| ---------------------------------------------------------------------------------------------- | ------------ | --------- |
| Waiting for some data                                                                          |      1       |     1     |
| Take a look at the MAC address when some data comes; verify if it should be here               |      1       |     1     |
| Look at the frame check sequence                                                               |      1       |     2     |
| Check the entire frame                                                                         |      1       |     2     |
| Strip the MAC address and metadata and keep the info                                           |      1       |     2     |
| Deal with IP addresses; check if the IP is correct and pass it further if it is                |      2       |     3     |
| Act as the assembler and disassembler of data: make data managable (remove sequencing numbers) |      3       |     4     |
| Connect a server to a client on a remote system                                                |      4       |     5     |
| Make data presentable (obsolete)                                                               |      4       |     6     |
| Built-in smarts that allow apps to interface to a network, resolve ports                       |      4       |     7     |

#### Server to client example

| Flow                                                                                   | TCP/IP stage | OSI stage  |
| -------------------------------------------------------------------------------------- | ------------ | ---------- |
| Take the data from the incoming frames and reverse the ports, present, etc.            |      4       | 7, 6 and 5 |
| Get the sequencing numbers, break up the data to packet size (make segment for TCP)    |      3       |      4     |
| Take the IP information and reverse it                                                 |      2       |      3     |
| Put on the MAC address, run a frame check sequence and send it                         |      1       |      2     |

## Meet the frame

*NIC* - Network Interface Card  \ These 2 make up the
The NIC is connected to a *hub* / *Local area network (LAN)*

> Data is not sent in big streams, but rather in discrete chunks (**frames** or **packets**) [of 1's and 0's]. The data is ***packetized***
> A single frame can be up to 1500 bytes long (or 12000 bits of data)
? Frames are created and destroyed inside the *NIC*

## The MAC address

***MAC*** - Media Access Control; sometimes called the *Physical address*
How do frames know how to get to the right computer?

A MAC address is a number of hex chars [separated by a hyphen (-)]. It's also a unique 48-bit identifier for a NIC
Mike's MAC (S3 L6): 40-8D-5C-1C-5A-50
Each hexadecimal character represents 4 binary characters
The first 3 groups are indicative of the type of router the computer is connected to, and they are refered to as unique OEM identified
The last digits are given random values (random for our purpose)
MAC addresses are added to the frame (own and where the data is going)
*CRC (cyclic redundancy check)* is also added. It's used to verify that the data is good. Bad data is resent

## Broadcase vs Unicast

MAC is sent along with data
Upon arrival, own MAC is not needed, but the sender's MAC is stored
> This is called *Unicast* (sending data to a singular machine)

The receiver's MAC is changed from their own to all F's (S2 L7), e.g FF-FF-FF-FF-FF-FF
Every computer that gets the information in this way will accept it
> This is called *Broadcast* (sending data to all devices in a broadcast domain)

Broadcast domain - machines that can hear each other's broadcast are in the same domain 

## Introduction to IP Addressing

As networks get bigger, we need to add another type of addressing called **logical addressing**
The most popular version of logical addressing used today is called ***IP Addressing***
They're not fixed with a network card

IP is 4 groups of numbers, separated by dots [.] (up to 255) with the first 3 being identical for the computers on the same network, and the 4th number differing.
A different network will have a different *network ID* (the first 3 groups)
**Router** is used to tie the IP and the MAC addresses together.
> Router is mounted onto a switch or already comes with the switch built in. It connects multiple LANs.

Two different networks can be connected using a router and a switch.
If a computer from one group wants to exchange information with the computer from the other group, the IP address will be included in the frame.


###### Frame with IP

Two networks connected via a single router

The first frame has:
1. MAC address of the destination
1. MAC address of the sender
1. CRC
1. The actual data

The frame with IP has:
1. MAC address of the **destination router**
1. MAC address of the sender
1. Destination IP address
1. Source IP address
1. CRC
1. The actual data

The IP's and the data constitute an **IP packet**.

If the IP didn't come from own network, the **default gateway** steps into action.
The default gateway is invariably the connection to the router itself.

Once the frame with IP gets to the router, the router strips away the excess stuff (MACs and CRC), leaving just the IP packet.
Using the **routing table**, the router will know where to send the data

> The routing table's job is to determine *where exactly* to send the data, based on the network information

The router will then reassemble the data, adding the recipients and own MACs and the CRC and send it.
Even though the frame was changed a couple of times, the IP packet still remains the same!

## Packets and ports

Two more pieces of information will need to be added: ***the port numbers***
They are unique to the individual applications using them (e.g PORT 80 is for HTTP)
The ports and the IP addresses will switch places and get sent back.

> The port range is 0 - 65535, but the first 1024 are reserved (for privileged users, like root/admin, etc)

Data travels in packs of smaller size, so that's where TCP steps in.

*Transmition Control Protocol (TCP)* is a connection-oriented conversation.
Two big pieces of TCP are a *sequencing number* and an *acknowledgement number*

The *User Datagram Protocol (UDP)* is similar to TCP, but with a glaring difference: 
**UDP is connectionless**; the application is supposed to determine whether the data comes to a computer in good order

