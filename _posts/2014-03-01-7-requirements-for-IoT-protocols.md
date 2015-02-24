---
title: "7 Essential requirements for the future protocol of the IoT"
date: 2014-03-01
tags: Tech IoT
---

Technology to pave the way for the Internet of Things has come a long way. The first frontier, getting an IP-Connection on the device, can be considered as finally crossed. [Cheap RF-Modules](http://vsaw-blog.blogspot.de/2013/12/6-simple-ways-to-add-wifi-to-your.html) and powerful Operating systems are widely available now so that the focus has shifted onto the data transport. Lately [a heated debate](http://blogs.cisco.com/ioe/beyond-mqtt-a-cisco-view-on-iot-protocols/) raised the question what protocol is most suitable. However so far I did not come across a list of requirements for the "IoT Protocol". So I gave it some thought and identified **7 essential requirements for data transport of (residential) Internet of Things applications**. Please note that I focused on the data transfer assuming there already is a (secure) TCP/UDP connection. So establishing a secure channel was left out on purpose.

I'd be happy to spark of a debate and hear some other opinions about what a protocol needs to acheive in order to power the Internet of Things! In the next post I will examine how well each of the most prominent protocols meet these requirements.

# 1. Decoupling of producer and consumers of data
A device that generates sensor readings or other sorts of data must not need to know all the consumers of the data. It should just broadcast the data throughout the system and who ever is interested in it will listen for the transmission and act on it. Otherwise, with changing reachability of sleeping devices it will be impossible for devices to request updates from a certain device.

# 2. Decentralized Link Local Communication
For reliable operation the system must be able to work even if certain devices or infrastructure fail. If the Internet connection at home breaks the devices should still be able to communicate locally with each other in the absence of the server.

A really well designed system would eliminate any single point of failure. That would include the WiFi access point. Instead the devices should form a peer-to-peer mesh network.

# 3. Real-Time event capable
Lot of applications will need to kick off action depending on certain events. These information has to be transmitted immediately and as fast as possible, because no one wants to wait 30 seconds for the next poll-cycle until finally the lights come on.

# 4. Delayed delivery
But just as much as the "push-event" capability I mentioned in the previous point the system will also need to be able to cope with devices that are not always receiving. Phones without a signal, or battery operated devices will often be in a state where they are not reachable. In this case messages for the device should be retained by the system/protocol and delivered to the the device as soon as it comes online.

# 5. Guaranteed delivery
Together with delayed messages the systems needs some Quality of Service where certain important messages can be reliably delivered. So that it knows that the data was processed by the system and will be delivered to the connected nodes. Optionally the sender should get some confirmation that his message was received by all devices.

# 6. Message ordering
It will be important to ensure that devices know what the recent data is so that they are not following outdated commands or readings. Also the same set of events can be handled differently depending on the order in which they happened. Imagine the simple case of someone coming home or leaving the house. Both will be captured by the same sensors but in a different order and both will have to be handled completely different. However with IP networks it is not guaranteed that the packets arrive in the correct order so the protocol has to synchronize and order them.

# 7. Data agnostic
That's a very obvious one because these requirements are shared across a wide range of devices so the protocol has to be agnostic of the application and transferred data.
