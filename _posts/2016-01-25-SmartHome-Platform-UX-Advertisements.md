---
title: Smart Home Platforms - Bringing IoT, the User and the Web industries closer together
tags: IoT
excerpt_separator: <!--more-->
---

<!-- Intro
Weave around the corner homekit been there a while so let's look at some implications of a smart home platform besides interoperability
-->
<!-- TODO links homekit and weave -->
A lot has been already said about SmartHome platforms, however the discussion mostly focuses on the interoperability and how it will make various devices work together. The most prominent and probably biggest platforms being [Google Weave](https://developers.google.com/weave/) and [Apple HomeKit](https://www.apple.com/ios/homekit/). With the release of Weave in the coming months I thought it's time to highlight some of the implications that have not been mentioned much: Guest access to improve user focus and marketing based on devices discovered on the home network. Especially how it will grow the consumer IoT closer mobile and web industries.

<!-- User focused Guest access
Quick talk how WiFi can replace the Registration and provide easy to use guest access
-->
## User focus and guest access
<!-- Dedicated Apps suck, each has their own user account and setup/rights management -->
<!-- Imagine a hotel room, the experience as a guest would suck -->
<!-- with a platform the situation could be different through umbrella apps -->
<!-- together with discovery it allows for users to take their preferences with them -->
Besides allowing devices to work easier with each other a common SmartHome platform will also allow users to easy interact the devices. Right now to control the appliances dedicated apps are required, each with their own set up and user accounts. While this might be okay for the "home" where set up only happens once, this is terrible for places like in hotel room. Just imagine installing 3 different apps to change the temperature, TV channel and unlock the door. A common platform would allow for umbrella apps that might already come pre-installed on your phone and give access to basic functionality of the devices. If combined with a guest access in the sense of "anyone on the same WiFi as the lights can turn them on/off" this will improve the usability a great deal. Together with a discovery feature, the phone could automatically send your preferences to the devices as soon as you connect to the hotel WiFi, and thus put the users needs in the center of the hotel experience.

## Device Discovery Marketing
<!-- App store asset management
The platforms will also provide some firmware info and probably even do a firmware update. App and device manufacturers will through the phone get info on the customers hardware and can find clues on usage and possible integrations. This will be competition for companies like DevicePilot and such
-->
<!-- Besides automatic preferences discovery has more value -->
<!-- One can find out what devices are installed, what FW they are running -->
<!-- Helps SW developer and manufacturers to understand their user base -->
<!-- Advertisers might also profit on knowing which devices might be missing in a home -->
Another important aspect of device discovery is that this information is of value to many more people. The phone and any other devices on the platform will be able to find out what other devices are there and probably also details on manufacturers, model, software version, etc. This information can then be evaluated in different ways:

- Manufacturers and independent software providers will be interested on the size and status of their installed base. They can learn in what kind of homes these devices are installed and identify possible integrations with other devices and prioritize features
- Advertisers can use this information to find potential customers. Think of it as a "Homes who have this device also have this device" to advertise interesting products.

Deployment statistics for apps are already collected in the App Stores of Google and Apple, therefore I suspect them to collect such statistics as well sooner or later. And for those manufacturers or advertisers who are not happy with the data collected by the built in mechanism will have to option to deploy code on devices to collect data independently, similar to todays 3rd Party Tracking Cookies on the Web.

## Consumer Privacy Consequences

From a consumer perspective such data must be handled with care to respect user privacy. As a wild prediction it could be that internet routers will soon have a Firewall that forbids certain devices to talk to each other, similar to Ad-Blockers in the Browser. In any case, such a platform will change the business of the consumer IoT and make it grow closer to mobile and web industries.
