---
title: "6 simple ways to add WiFi to your Internet of Things device"
tags: Tech IoT
---

Wireless connectivity has finally become a commodity! There are many modules that can be used of the shelf to add wireless connectivity to your Internet of Things devices. In this post I'll cover some of the simplest ways to build a WiFi connected device.

First if you want to start from the ground, these are platforms that come with WiFi out of the Box:

- [Raspberry Pi](http://www.raspberrypi.org/quick-start-guide): The famous Raspberry Pi is a computer the size of a credit card. Although it does not come with a WiFi Module you can easily [pick any USB WiFi from Amazon](http://www.amazon.com/s?ie=UTF8&field-keywords=usb%20wifi&index=blended) and plug it in. Done! Your Pi is now WiFi enabled and you are ready to start working on your App and not the Networking.
- [ArduinoWiFiShield](http://arduino.cc/en/Main/ArduinoWiFiShield): If you are an Arduino Afficionado this WiFi shield will get you off the ground.
- [Spark Core](https://www.spark.io/): Being fully Arduino compatible the Spark Core takes WiFi connectivity to a different level by providing powerful Cloud Services that will help you manage your devices once deployed. The [Spark Build](http://docs.spark.io/#/start/writing-core-firmware-spark-build-our-web-ide) Web IDE for example enables you to fully reprogram the Spark Core over the Internet.
- [Electric Imp](http://electricimp.com/): The cool thing about the Imp is, besides that it's the size of an SD-Card, that it comes with [BlinkUp](http://electricimp.com/docs/gettingstarted/1-blinkup/), a simple way to enter the WiFi credentials into devices that do not have a user interface. All you need is your Phone which will then "blink" them to the Imp.

And in case you already have a device and are looking for simple ways to add WiFi, try these:

- [TI CC3000](http://www.ti.com/product/cc3000): When looking for a way to connect existing products to the internet without having to deal with Networking to much the CC3000 could be worth a look. It is a networking co-processor that handles all the WiFi and IP troubles so that the main application processor can send and receive raw data through the CC3000. Plus, like the Electric Imp it comes with a way to painlessly enter WiFi credentials called [Smart Config](http://processors.wiki.ti.com/index.php/CC3000_Smart_Config).
- [Murata SN8200](http://processors.wiki.ti.com/index.php/CC3000_Smart_Config): Modules like the SN8200 take the network co-processor design a step further by not only taking care of WiFi and IP but also application layer protocols like HTTP. It gets as easy as telling the SN8200 to open http://vsaw-blog.blogspot.de/ and then wait for the page to arrive over UART. Compared to the CC3000 it has an intergrated antenna, so no RF design necessary. The SN8200 is powered by the [Wiced SDK](http://www.broadcom.com/products/wiced/wifi/) which comes with a lot of good stuff like a full SSL/TLS implementation.

If you think I'm missing something please leave a comment! I'd love to see this list grow over time.
