---
title: "Brains, muscles, eyes & ears - A simple way to describe and design a real word sensor/actuator system"
tags: Tech IoT
---

While in the process of brainstorming an improved architecture for "regular" sensor/actuator systems it came to me how hard it actually is to come up with a clean scheme for such things.The design quickly becomes something where Information, roles and states of the Devices/Agents get mixed into a complex mess! Which is not surprising since in the end there are many interconnected agents forming a larger system.

So to simplify the process of designing such a system I propose a "low-tech" modelling scheme which I believe can help setting the right frame to define a common language to describe and express what even the most complex system should or should not do:

# Brains, Muscles, Eyes & Ears
Essentially there are 3 types that each component of the system belongs to. I will quickly explain each role with a typical use case from the home-automation: climate control.

- **Eyes & Ears**: They are collecting data, performing measurements and communicate what they perceive to all other components. In a heating system these could be temperature sensor in each room of the home. But this could also be a weather forecast from the internet or the residents location transmitted from their phone.
- **Brain**: The Brain is where the intelligence sits. It gets the information from the eyes & ears and thinks about what to do next. It can be implemented in a device in the home or in the cloud. This does not make much of a difference as long as the brain has a reliable way to talk to the Muscles.
- **Muscles**: Muscles are the only one that have actual physical impact on the real world. Actions of the muscles have an impact on the readings of the eyes & ears. For examples in heating the thermostatic radiator valves or the room thermostat could be the muscles.

For simplicity assume that there is a house with a separate device for each role. So there is one temperature sensor, one thermostat and both are connected to a smart brain in the cloud. But of course they could be combined e.g. if the brain is in the home it could be able to do measurements as well.

# Communication between the 3
- **Eyes & Ears with the Rest**: Ideally, the eyes & ears tell everything they see and hear to the rest. The rest in this case means anyone that needs this information and can be trusted with it. Trust and a secure communication channel will have to be established beforehand between the devices. However I can see that the brain or the muscles might not be interested in everything that happens. So they could tell what information they are interested in. There also might be technical limitations to set filters to limit transmission.
- **Brain and Muscles**: The conversation between the brain and the muscles is in it's essence very straightforward. The brain tells the muscles what to do (but NOT how to do it) and the muscles keep the brain up to date with what they are currently doing to meet goals the brain has set. It is important to understand why the brain must not tell the muscles how to do everything. The muscle needs to have some autonomy with regards to his actions because of two simple reasons:
  1. If the brain and the muscle for some reason can not talk to each other, the muscle is still smart enough to at least do something. It has the power and the knowledge to follow some "emergency protocol" until communication is restored.
  2. It hides the implementation of the muscle from the brain. In the heating example it could be that different boilers require different electrical interfaces and therefore different muscles. Hiding this from the brain allows for much greater flexibility.

# The role of the user
The user could have any of the roles and also change roles over time for example:

- **Eyes & Ears**: The brain could ask the user if he is comfortable with the current climate. In this case the user is just another "sensor".
Brain: The user could also be a manual override and command the brain what to tell the muscles.
- **Muscles**: The brain could ask the user for help in situations where is does not have a muscle to take care of it, for example the brain could ask the user to open a window if the air humidity is to high.

The nice thing about putting the user in the same roles is that the duties could also be delegated from the user to a different entity. For example put a motor to the window and now the brain can control the muscle directly without having to ask the user. This gives a nice way to also describe user interaction within the simple model that is used to describe the rest of the system.
