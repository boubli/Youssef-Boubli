---
layout: article
title: "Wifi Jammer using NodMCU ESP8266"
date: 2019-01-14 12:45:00+0200
coverPhoto: https://miro.medium.com/max/946/1*SmScNHqJkUIhbfnSb7SO0w.jpeg
---

![](https://github.com/boubli/Youssef-Boubli/blob/gh-pages/contents/images/2019/01/51076992-b390e100-1697-11e9-9be1-ed5c63a067a6.png?raw=true)

NodeMCU is an open source IoT platform It includes firmware which runs on the ESP8266 Wi-Fi SoC from Espressif Systems, and hardware which is based on the ESP-12 module. The term "NodeMCU" by default refers to the firmware rather than the development kits. The firmware uses the Lua scripting language. It is based on the eLua project, and built on the Espressif Non-OS SDK for ESP8266. It uses many open source projects, such as lua-cjson[8] and SPIFFS.

`Download source code` [Here](https://github.com/boubli/Wifi-Jammer-NodeMCU/archive/master.zip)

<iframe width="873" height="512" src="https://www.youtube.com/embed/zD2M8a9pqCM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

![](https://github.com/boubli/Youssef-Boubli/blob/gh-pages/contents/images/2019/01/Screen%20Shot%202019-01-14%20at%2012.50.01%20AM.png?raw=true)

NodeMCU is an open source IoT platform It includes firmware which runs on the ESP8266 Wi-Fi SoC from Espressif Systems, and hardware which is based on the ESP-12 module. The term "NodeMCU" by default refers to the firmware rather than the development kits. The firmware uses the Lua scripting language. It is based on the eLua project, and built on the Espressif Non-OS SDK for ESP8266. It uses many open source projects, such as lua-cjson[8] and SPIFFS.

![](https://github.com/boubli/Youssef-Boubli/blob/gh-pages/contents/images/2019/01/Screen%20Shot%202019-01-13%20at%2011.12.02%20PM.png?raw=true)

`Download source code` [Here](https://github.com/boubli/Wifi-Jammer-NodeMCU/archive/master.zip)


<center><iframe width="600" height="300" src="https://www.youtube.com/embed/zD2M8a9pqCM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

{% highlight html %}

	http://arduino.esp8266.com/stable/package_esp8266com_index.json

	typedef void (*freedom_outside_cb_t)(uint8 status);
	int wifi_register_send_pkt_freedom_cb(freedom_outside_cb_t cb);
	void wifi_unregister_send_pkt_freedom_cb(void);
	int wifi_send_pkt_freedom(uint8 *buf, int len, bool sys_seq);

{% endhighlight %}

## Falsh ESP8266 
 * open esptool file to flash EPS8266 all you need to do is open Termianl in Mac or cmd in Windows

 `esptool.py --port /dev/ttyUSB0 write_flash --flash_mode qio --flash_size 4MB 0x0 bootloader.bin 0x1000 my_app.bin`


 

