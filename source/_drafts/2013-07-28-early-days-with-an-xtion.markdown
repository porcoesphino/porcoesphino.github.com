---
layout: post
title: "Early days with an Xtion"
date: 2013-07-28 11:36
comments: true
categories: 
- Nerdy
- Point Clouds
- Xtion
---

I'm about to start working with an Xtion and some point cloud work. First step is to get it running on my machine. It looks like there are a few packages around for OS X like these:
- Hmm?

I've just recently made my box all pretty with Boxen (I had to change hard drives anyway) and I don't want a mess installed all through root owned directories. So, my first step is to install on a virtual machine. The linux instructions are far better documented anyway so I'll start there. I was hoping to have played with vagrant more before now, but I'll just have to make do.

From what I can see, the instructions are:
1 Install OpenNI (unstable version v 1.5.4.0) from http://openni.org/Downloads/OpenNIModules.aspx .
2 Install hardware binaries (stable version v 5.1.041) from http://openni.org/Downloads/OpenNIModules.aspx
3 Try NiViewer and pcl OpenNIGrabber

Alternatively:
- Install OpenNI.
- Install Sensor Driver.
- Install Nite.
- Run the NiViewer under the sample folder in the OpenNI folder to test the camera. You can right click your mouse to change settings.
- http://openni.org/Documentation/Tutorial/smpl_simple_view.html includes some useful samples to start working on.
- If you haven’t heard of PCL, http://pointclouds.org/ provides a large set of libraries on handling point clouds, and also a visualizer for viewing them in 3D. If you use PCL, it already provides an interface “OpenNIGrabber” to retrieve point clouds or color point clouds.

The bmwesting/KinectArray project on GitHub lists these:
 - OpenNI (http://www.openni.org/)
 - VTK 5.4+ (http://www.vtk.org/)
 - Kinect Sensor Module for OpenNI:
   - Linux & Mac & Win32 (https://github.com/avin2/SensorKinect)
 - PrimeSense Sensor Module for OpenNI:
 - Windows and Ubuntu Linux (http://www.openni.org/downloadfiles/opennimodules/openni-compliant-hardware-binaries/32-stable)

NOTE: One post mentioned issues if the camera wasn't run at 320x240

Prerequisites: mono-complete libusb-1.0-0-dev freeglut3-dev
Mac: libtool libusb-dev
