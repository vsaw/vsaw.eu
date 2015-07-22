---
title: "Physical Security in the IoT"
tags: IoT IT-Security Tech
---

<!-- Physical Security way more expensive for very robust widespread implementations to keep 30bn devices safe -->
Security in the IoT is still a very active topic. Work is being done on all aspects of the IoT, the network, the data but also on the physical level?

*Physical Security* is concerned with protecting the device internal and external hardware. It aims to ensure the integrity of the deployed hardware and prevent unauthorized access to privileged manufacturing and debugging interfaces against attackers with direct physical access to the hardware. So naturally it involves sturdy enclosures, mechanic locks and such, all of which is expensive to manufacture.

## How much of the IoT requires physical security?
<!-- Loads of times not required (home based devices) -->
In many cases, devices do not require strict physical, as physical access to the device already indicates a bigger problem that should have prevented. Consider consumer IoT in the home for example. Here unauthorized physical access to a device already means having a burglar in the home, which by itself is a bigger problem. So the threat model for these devices will be to rely on the "access control" of the home itself.

<!-- 30bn devices are to expensive to update -->
<!-- Only devices that already receive service and maintenance will receive
Hardware-Securiy Updates -->
Therefore only device is an untrusted environment (mainly public environment) need physical security. Considering the large number of billions of devices to be deployed in the coming years enormous costs will have to be payed for high physical security. Therefore it can be expected that only a best effort of physical security will be implemented to stop some attacks. Dedicated attackers however will still be able to break the security measures in place. Only very few high value targets, where failure is very expensive, will receive continuous hardware updates.

<!-- Thread Model: Expect things to be hacked but don't break the net or reveal sensitive information on the device -->
## Damage Control Thread Model
Since hardware integrity can not be guaranteed the thread model needs to adjusted. To incorporate the following two principles

1. Expect hardware to be broken
2. Don't blindly trust devices on the network

This has very important consequences for the design of the rest of the system. For example not to store sensitive information on the devices, which could otherwise be read by the attacker. Or that sophisticated attacks could try hijack devices to gain access to the network, therefore the whole system must be designed, that a security breach in one device must not bring the whole network down.
