---
title: "Phone Data Leakage Through Unprivileged Sensor Access"
tags: Tech IT-Security
excerpt_separator: <!--more-->
---

Access to physical Sensors like Acceleration and Orientation/Gyroscope is considered unprivileged on Android Phones. Most likely because the data captured by these sensors is considered not harmful or sensitive.

However analysis of sensor data from the device quickly reveals that certain device usage patterns are clearly visible. The most sophisticated attack known to me even shows that a tap-logger can be built which records any user interaction with the screen.
<!--more-->

# Leaked Data
First an Overview of the data that I know can be leaked through unprivileged sensors.

![Vibration and Typing](/assets/posts/2015-04-03-Phone-Data-Leakage-Through-Unprivileged-Sensor-Access/sms_and_typing.png)

The green peaks on the left show the devices vibration on the reception of a text message while the following read peaks show user input on the on screen keyboard.

However the most sophisticated attack I know of today is performed by Zhi Xu, Kun Bai and Sencun Zhu in their [TapLogger: Inferring User Inputs On Smartphone Touchscreens Using On-board Motion Sensors](http://www.cse.psu.edu/~szhu/papers/taplogger.pdf) Paper. They combine acceleration and gyroscope data to infer the position of the on-screen touch.

# The TapLogger Attack
Zhi Xu, Kun Bai and Sencun Zhu show that little requirements are sufficient to build an remote TapLogger

- some decoy App for training the Model (e.g. some point and tap game)
- a background service with Internet Permission

Since Sensors can be accessed without the users permission these will be the only two user noticeable features of the TapLogger App. Both are very common and will not raise any concern from the user.

# Protection Measures
Since Sensor access can not be prevented (at least not in Android). The only known protection is to not leak information through vibration or gyroscope. Hence

- **Disable Vibration**: This leaks less phone usage patterns
- **Smaller on-screen keyboard**: Narrow taps are harder to tell apart
- **Desk Typing**: Keep the device perfectly still when typing sensitive data. Having it lying on the desk is already enough to prevent leaking gyroscope and most acceleration data

# Outlook
One things which is not clear to me yet and which I'd like to learn about is if this sensor data can be used to get insights about phone calls as well.

While doing phone calls the phone hold against your face and thus might be picking up movements of your lips and jaws. And I wonder if these movements can be used to train your phone to read your lips?
