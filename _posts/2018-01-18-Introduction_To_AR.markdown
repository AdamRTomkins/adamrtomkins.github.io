---
layout: post
title:  Introduction to AR Development
date: 2018-01-05 13:00:00
description: An introduction to the technologies behind Augmented reality, and where to start developing.
---
[Warning, this is part of an ongoing Augmented Reality series, expect changes regularly]

## An Introduction to Augmented Reality

This post is a short review of the augmented reality development space, with the aim of giving you a broad overview of the hardware and software choices you can make before starting development. 

### What is Augmented Reality

Augmented reality is the art of mixing virtual elements into a physical reality, as opposed to Virtual reality, where the entirety of the experience is digital, you inhabit another world.

In augmented reality you still squarely inhabit this world, but with additions overlaid on top.

There are two main types of augmented reality, which reflect the evolution in AR, Tracked and Trackerless.

Tracked AR uses an image or object than can be easily digitally recognised, and is tracked by the AR device, and used as place holder in the real world, this gives you a place in the world that you can overlay your digital images. In its purest form, this is the easiest AR to build, and can be very effective, but has several drawbacks. You can find my first tutorial on tracked AR in Vuforia (here)[..]

Trackerless AR is more complicated, and uses more computationally intensive methods to profile the real world, and extract areas of interest, such as flat planes( a table or the floor). This information can then be used to more intelligently add digital overlays, such as a cat walking around the floor, or plants growing on the table. The latest AR libraries from Google (ARCore) and Apple (ARKit) are capable of this kind of trackerless AR experience.


### AR Technology Stacks

There are several easily accessible ways to develop an AR application, with some very capable software libraries.

1. Vuforia
2. ARCore
3. ARKit
4. ARjs and A-Frame

#### Vuforia

My first experiences with AR was with Vuforia, and it has a free developer tier which makes it great to easily get involved with. Since my initial forays into AR with Vuroria, it has since been integrated directly into Unity, making your first AR experience a doddle.

#### ARjs and A-Frame

In contrast to the full development environment of Unity+Vuforia, you can easily build your first AR experience in HTML, using ARjs as the library to detect and overlay images, and A-Frame as a great framework for AR and VR graphics in the browser. I think this is a great way to get involved with a more technologically conservative platform, and I'll have a tutorial up for this shortly.

#### ARCore and ARKit

These are the big guns and the new contenders, which promise a more in-depth look at AR. Both of these can be used in conjunction with Unity, making for an integrated AR development experience. ARCore is focused on Android devices, and ARKit on Apple. However as they demand a more capable hardware set up than Vuforia, they will be left to last in the tutorial session, but they are a promising route to fully functional AR, especially with support for dynamic lighting.


### AR Hardware

The AR space is not as developed as the VR Space with dedicated VR Headsets and Mobile Headsets, but there are commercially available units that we can use to get started with AR technology.

The big players in the space are Microsoft with the Hololens, and Meta with the Meta2 headset. While these are promising, they are hard to get hold of and expensive, especially as a fledgling AR developer.

We will focus on the Mobile AR development, which gives you two options, hand-held mobile AR, and Cardboard style AR headsets, such as the Aryzon. You can find the getting started tutorials with both, using Vuforia (here)[..] and (here)[..]

