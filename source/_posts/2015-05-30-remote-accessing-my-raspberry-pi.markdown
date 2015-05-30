---
layout: post
title: "Remotely Accessing My Raspberry Pi"
date: 2015-05-30 11:32:11 +0100
comments: false
categories: technical
---
{% img right /images/logo-black-pi.png 100 100 %}
Here's a few programs I use to enable remote control/access of my Raspberry Pi.
<!--more-->

**NOTE:** My Pi is running the Raspian OS, a modified Debian Weezy.

---
**SSH** </br>
My Pi starts a [SSH (Secure SHell)](http://www.openssh.com/index.html) server at bootup by default. I connect to this server using [PuTTY](http://www.putty.org) a SSH client freely available for most OS/devices. PuTTY provides a command line console where you remotely login to the Pi and issue commands.

---
**VNC** </br>
I'm using [TightVNC](http://www.tightvnc.com/) to remotely access the Pi's Desktop. See [VNC (Virtual Network Computing)](https://www.raspberrypi.org/documentation/remote-access/vnc/README.md). Once the server is setup on the Pi you'll be able to connect to it with a VNC-Viewer, which are freely available for most OS/devices.

---
**SFTP** </br>
The best free FTP client is [FileZilla](https://filezilla-project.org/download.php). I use this if I need to copy many files to the Pi.

---
**Samba** </br>
[Samba](https://www.samba.org/) provideds secure, stable and fast file services, amongst other things. Installing the server on the Pi is quite straight forward, I used [this article at HowToGeek](http://www.howtogeek.com/139433/how-to-turn-a-raspberry-pi-into-a-low-power-network-storage-device/) as a reference.

I used a 8GB UFD for my ../shares/ folder. I had problems getting permissions right for ../shares/. A solution was to clean format the UFD to ext4 using [Gparted](http://gparted.sourceforge.net/) then create the shares folder and set the correct permissions all on another linux system.

I can now access the RASPBERRYPI shares folder from either Windows or Linux.

---
[Raspbery Pi Documentation](https://www.raspberrypi.org/documentation/remote-access/README.md)</br>
[Samba on HowToGeek](http://www.howtogeek.com/139433/how-to-turn-a-raspberry-pi-into-a-low-power-network-storage-device/)
