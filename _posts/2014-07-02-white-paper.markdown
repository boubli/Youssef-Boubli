---
layout: article
title: "100-105 Passing Guarantee Exam"
date: 2014-07-02 11:09:00+0200
coverPhoto: https://image.slidesharecdn.com/100-105ciscoexam-100passingguaranteewithlatestdemo-170530105821/95/100105-cisco-exam-100-passing-guarantee-with-latest-demo-1-638.jpg?cb=1496141942
---



Question: 1

Which three statements are true about the operation of a full-duplex Ethernet network? (Choose three.)

A. There are no collisions in full-duplex mode.
B. A dedicated switch port is required for each full-duplex node.
C. Ethernet hub ports are preconfigured for full-duplex mode.
D. In a full-duplex environment, the host network card must check for the availability of the network media before transmitting.
E. The host network card and the switch port must be capable of operating in full-duplex mode.

Answer: A, B, E 

Explanation:
Half-duplex Ethernet is defined in the original 802.3 Ethernet and Cisco says you only use one wire pair with a digital signal running in both directions on the wire. It also uses the CSMA/CD protocol to help prevent collisions and to permit retransmitting if a collision does occur. If a hub is attached to a switch, it must operate in half-duplex mode because the end stations must be able to detect collisions. Half-duplex Ethernet—typically 10BaseT—is only about 30 to 40 percent efficient as Cisco sees it, because a large 10BaseT network will usually only give you 3- to 4Mbps—at most.
Full-duplex Ethernet uses two pairs of wires, instead of one wire pair like half duplex. Also, full duplex uses a point-to-point connection between the transmitter of the transmitting device and the receiver of the receiving device, which means that with full-duplex data transfer, you get a faster data transfer compared to half duplex. And because the transmitted data is sent on a different set of wires than the received data, no collisions occur. The reason you don’t need to worry about collisions is because now Full-duplex Ethernet is like a freeway with multiple lanes instead of the single-lane road provided by half duplex. Full-duplex Ethernet is supposed to offer 100 percent efficiency in both directions; this means you can get 20Mbps with a 10Mbps Ethernet running full duplex, or 200Mbps for FastEthernet.

Question: 2

DRAG DROP
On the left are various network protocols. On the right are the layers of the TCP/IP model. Assuming a reliable connection is required, move the protocols on the left to the TCP/IP layers on the right to show the proper encapsulation for an email message sent by a host on a LAN. (Not all options are used.)

Answer: 

Question: 3
Which OSI layer header contains the address of a destination host that is on another network?

A. application
B. session
C. transport
D. network
E. data link
F. physical

Answer: D 

Explanation:
Only network address contains this information. To transmit the packets the sender uses network address and datalink address. But the layer 2 address represents just the address of the next hop device on the way to the sender. It is changed on each hop. Network address remains the same.

Question: 4

Which layer of the TCP/IP stack combines the OSI model physical and data link layers?

A. Internet layer
B. transport layer
C. application layer
D. network access layer

Answer: D 

Explanation:
The Internet Protocol Suite, TCP/IP, is a suite of protocols used for communication over the internet. The TCP/ IP model was created after the OSI 7 layer model for two major reasons. First, the foundation of the Internet was built using the TCP/IP suite and through the spread of the World Wide Web and Internet, TCP/IP has been preferred. Second, a project researched by the Department of Defense (DOD) consisted of creating the TCP/IP protocols. The DOD's goal was to bring international standards which could not be met by the OSI model.
Since the DOD was the largest software consumer and they preferred the TCP/IP suite, most vendors used this model rather than the OSI. Below is a side by side comparison of the TCP/IP and OSI models.

Question: 5

Which protocol uses a connection-oriented service to deliver files between end systems?

A. TFTP
B. DNS
C. FTP
D. SNMP
E. RIP

Answer: C 

Explanation:
TCP is an example of a connection-oriented protocol. It requires a logical connection to be established between the two processes before data is exchanged. The connection must be maintained during the entire time that communication is taking place, then released afterwards. The process is much like a telephone call, where a virtual circuit is established--the caller must know the person's telephone number and the phone must be answered--before the message can be delivered.
TCP/IP is also a connection-oriented transport with orderly release. With orderly release, any data remaining in the buffer is sent before the connection is terminated. The release is accomplished in a three-way handshake between client and server processes. The connection-oriented protocols in the OSI protocol suite, on the other hand, do not support orderly release. Applications perform any handshake necessary for ensuring orderly release.
Examples of services that use connection-oriented transport services are telnet, rlogin, and ftp.

Question: 6

Refer to the exhibit.

If the hubs in the graphic were replaced by switches, what would be virtually eliminated?

A. broadcast domains
B. repeater domains
C. Ethernet collisions
D. signal amplification
E. Ethernet broadcasts

Answer: C 

Explanation:
Modern wired networks use a network switch to eliminate collisions. By connecting each device directly to a port on the switch, either each port on a switch becomes its own collision domain (in the case of half duplex links) or the possibility of collisions is eliminated entirely in the case of full duplex links.

Question: 7

Refer to the exhibit.

If host A sends an IP packet to host B, what will the source physical address be in the frame when it reaches host B?

A. 10.168.10.99
B. 10.168.11.88
C. A1:A1:A1:A1:A1:A1
D. B2:B2:B2:B2:B2:B2
E. C3:C3:C3:C3:C3:C3
F. D4:D4:D4:D4:D4:D4

Answer: E 

Explanation:
When packets transfer from one host to another across a routed segment, the source IP address always remains the same source IP address, and the source physical (MAC) address will be the existing router’s interface address. Similarly, the destination IP address always remains the same and the destination physical (MAC) address is the destination router’s interface address.

Question: 8

Refer to the exhibit.

HostX is transferring a file to the FTP server. Point A represents the frame as it goes toward the Toronto router. What will the Layer 2 destination address be at this point?

A. abcd.1123.0045
B. 192.168.7.17
C. aabb.5555.2222
D. 192.168.1.1
E. abcd.2246.0035

Answer: E 

Explanation:
For packets destined to a host on another IP network, the destination MAC address will be the LAN interface of the router. Since the FTP server lies on a different network, the host will know to send the frame to its default gateway, which is Toronto.

Question: 9

Which network device functions only at Layer 1 of the OSI model?

A. Option A
B. Option B
C. Option C
D. Option D
E. Option E

Answer: B 

Explanation:
Most hubs are amplifying the electrical signal; therefore, they are really repeaters with several ports. Hubs and repeaters are Layer 1 (physical layer) devices.

Question: 10

Refer to the exhibit.

The host in Kiev sends a request for an HTML document to the server in Minsk. What will be the source IP address of the packet as it leaves the Kiev router?

A. 10.1.0.1
B. 10.1.0.5
C. 10.1.0.6
D. 10.1.0.14
E. 10.1.1.16
F. 10.1.2.8

Answer: E 

Although the source and destination MAC address will change as a packet traverses a network, the source and destination IP address will not unless network address translation (NAT) is being done, which is not the case here.