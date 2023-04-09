---
layout: page
permalink: /doc
title: LegoSENSE Basics
description: How does LegoSENSE work?
nav: true
nav_order: 5
---

### Hardware
* **Carrier Board** – The LegoSENSE is assembled by inserting a carrier board into the Raspberry Pi device, allowing the Raspberry Pi to interface sensing modules (module boards?) that are plugged into the carrier board. 
* **Modules** – Modules connect sensor(s) to the carrier board. LegoSENSE therefore eliminates the need for the user to fiddle with cables or other peripheral components of the Raspberry Pi itself. Modules will be equipped with a non-volatile memory chip that would be factory-programmed with the carrier board’s type, along with any calibration information for the sensor(s). This would be used to support plug-and-play functionality.
Software

### Software
* **Web Dashboard** - LegoSENSE employs a web server on the Raspberry Pi and makes all data flow in its pipeline through HTTP. First, the web server serves a web-based dashboard via which users may examine system status and sensor data in real time and adjust sensor configurations. The dashboard makes the system beginner-friendly by allowing the user to control the system by just clicking buttons on any web browser, even on smartphones. we also implement RESTful Application Programming Interface (API) within the web server to allow more advanced users to programmatically access the system via API calls  which makes further customization possible.

* **Plug and Play functionality** – In order to implement the plug-and-play functionality described in the hardware above, LegoSENSE’s software system uses a background service called the plug-and-play controller which periodically pulls data out of the non-volatile memory chips to identify the type of the module, and automatically obtains the driver for the module from a repository. 

