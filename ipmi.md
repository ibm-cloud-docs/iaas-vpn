---
copyright:
  years: 1994, 2017
lastupdated: "2018-07-23"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

## IPMI Concepts

Intelligent Platform Management Interface (IPMI) is an internet protocol, which went into use in 1998. It provides a way to “speak” directly to the hardware of your cloud, in a message-based communication style.

IPMI is intended primarily for use by system administrators.

IPMI lets a system administrator perform _out-of-band_ management, which means that a system can be monitored or altered in circumstances such as these:
 * before an OS has booted (allowing, for example, the remote monitoring or changing of BIOS settings)
 * when the system is powered down
 * after OS or system failure 

Out of band management can be conceptualized _as if_ you can “stop time” or work outside of time with your system’s components.

That’s the key characteristic of IPMI compared with in-band system management, such as by remote login to the operating system using SSH, which relies upon some running software, such as an operating system.

Here is a basic overview of the three steps in using IPMI:
 * you use some type of secure network login to reach your IPMI card or port, 
 * you log in with an account that has `admin` or `root` privileges,  
 * you boot the system or otherwise manage your servers.


Wikipedia has an excellent [article on IPMI](https://en.wikipedia.org/wiki/Intelligent_Platform_Management_Interface).
